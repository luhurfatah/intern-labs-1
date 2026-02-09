# Lab 13: Terragrunt Import

| Difficulty | Est. Time | Prerequisites |
|------------|-----------|---------------|
| Intermediate | 45 Mins | Lab 12, Lab 13|

## 🎯 Objectives
- Manually create AWS resources to simulate legacy infrastructure.
- Master the `terragrunt import` command.
- Understand how Terragrunt automatically manages remote state during an import.
- Codify existing resources into a DRY Terragrunt structure.

---

## 🗺️ The Terragrunt Import Workflow

```mermaid
graph TD
    Console[Manual Resource in Console] --> Config[Write root.hcl]
    Config --> Import[terragrunt import]
    Import --> Init[Auto-Init Backend]
    Init --> State[Update Remote State]
    State --> Plan[terragrunt plan]
    Plan -- "No Changes" --> Success[Codified!]
```

---

## 📚 Concepts

### 1. Why `terragrunt import`?
When using Terragrunt, you should always use its wrapper command instead of raw `terraform import`. 
- **Auto-Initialization**: Terragrunt ensures the S3 backend is ready before importing.
- **Remote State Sync**: It automatically places the imported resource into the correct state path based on your folder structure.

### 2. The Import Process
Importing into Terragrunt follows the same rule as Terraform: it only updates the **state**. You still need to provide the matching configuration for the resource to be fully managed.

---

## 🛠️ Step-by-Step Lab

### Step 1: Create Manual Resources
Go to the AWS Console and create the following "legacy" resources:
1.  **Security Group**: Name: `terragrunt-manual-sg`, Allow SSH (Port 22).
2.  **S3 Bucket**: Name: `terragrunt-manual-bucket-[yourname]` (must be unique).
3.  **EC2 Instance**: Launch a `t3.micro` named `manual-ec2` in the default VPC.

### Step 2: Setup Terragrunt Configuration
Navigate to your repository and create the following structure:
```text
dev/
├── security-group/
│   └── terragrunt.hcl
├── s3-bucket/
│   └── terragrunt.hcl
└── ec2-instance/
    └── terragrunt.hcl
```

Update each `terragrunt.hcl` to point to the respective modules, provide inputs that match your manual resources, and **include the root config**:

```hcl
include "root" {
  path = find_in_parent_folders("root.hcl")
}
```

### Step 3: Execute Import
Run the following commands from their respective folders:

**Security Group:**
```bash
terragrunt import aws_security_group.this_name_prefix[0] sg-xxxxxxxx
```

**S3 Bucket:**
```bash
terragrunt import aws_s3_bucket.this[0] terragrunt-manual-bucket-yourname
```

**EC2 Instance:**
```bash
terragrunt import aws_instance.this[0] i-xxxxxxxxxxxx
```

### Step 4: Verify and Modify (The "Real" Test)
How do you know Terragrunt is actually in control?

1.  **Modification**: Change a Tag in your `ec2-instance/terragrunt.hcl`:
    ```hcl
    inputs = {
      # ... existing inputs
      tags = {
        ManagedBy = "Terragrunt"
        Owner     = "[Your Name]"
      }
    }
    ```
2.  **Plan**: Run `terragrunt plan`. Observe that it wants to **update** the tags.
3.  **Apply**: Run `terragrunt apply`.
4.  **Confirm**: Check the AWS Console. Your EC2 instance should now have the new tags!

---

## ❓ Troubleshooting & Pitfalls

- **State Fragmentation**: Always use `terragrunt import` to ensure the S3 backend is used.
- **Module Internal Names**: Different modules use different internal names for resources (e.g., `this` vs `main`). Check the module's `main.tf` if the import fails.
- **Resource Dependencies**: If you import a VPC, remember to import its subnets and route tables too if you want full management.

---

## 🔥 BONUS CHALLENGE: The Move
**Scenario**: You want to move your manual resources into a different environment folder (e.g., from `dev/` to `staging/`).
1.  Copy the configuration to the new folder.
2.  Import the resources again into the new state.
3.  **Question**: What happens to the old state file?

---

## 🧹 Cleanup
Delete all resources using Terragrunt:
```bash
terragrunt run-all destroy
```

---

## 🧹 Cleanup
Delete the resource using Terragrunt:
```bash
terragrunt destroy
```
