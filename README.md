# ☁️ Cloud Engineer Intern Training (AWS + Terraform)

Welcome to the 2-week intensive training program. This repository is your central hub for both theory and practice. You will transition from manual AWS console operations to fully automated Infrastructure as Code (IaC) using Terraform and Terragrunt.

---

##  Table of Contents
1. [Module 0: Cloud Computing Fundamentals](#module-0-cloud-computing-fundamentals)
2. [Module 1: AWS Introduction & IAM](#module-1-aws-introduction--iam)
3. [Module 2: Virtual Private Cloud (VPC)](#module-2-virtual-private-cloud-vpc)
4. [Module 3: Compute & Storage](#module-3-compute--storage)
5. [Module 4: High Availability & Scaling](#module-4-high-availability--scaling)
6. [Module 5: Security & DNS](#module-5-security--dns)
7. [Module 6: Infrastructure as Code (Terraform & Terragrunt)](#module-6-infrastructure-as-code-terraform--terragrunt)
8. [Mentor Guides](#-mentor-guides)
9. [Cost Management](#-cost-management)

---

## Module 0: Cloud Computing Fundamentals
*Understanding the 'Why' behind Cloud Computing.*

- **Concepts**: What is Cloud Computing? Benefits of Cloud (Agility, Cost, Elasticity).
- **Resources**:
    - [Cloud Computing Fundamentals (Educative.io)](https://www.educative.io/courses/cloud-computing-fundamentals)
    - [Understanding Cloud Computing (DataCamp)](https://www.datacamp.com/courses/understanding-cloud-computing)
    - [Roadmap.sh AWS](https://roadmap.sh/aws)
    - [Cloud Computing Explained: The Most Important Concepts To Know](https://www.youtube.com/watch?v=ZaA0kNm18pE)
    - [AWS Educate](https://aws.amazon.com/education/awseducate/)

---

## Module 1: AWS Introduction & IAM
*Your first steps into the AWS ecosystem.*

- **Objectives**: Setup AWS CLI, understand Regions/AZs, and manage permissions.
- **Resources**:
    - [What is AWS? Explained in Plain English (Video)](https://www.youtube.com/watch?v=W6jQmVi31Xk)
    - [Getting Started with AWS Cloud Essentials (AWS Skill Builder)](https://skillbuilder.aws/learn/Y738EQQD49/getting-started-with-aws-cloud-essentials/YEWD5RAWZJ)
    - [AWS Cloud Practitioner Essentials](https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7)
    - [AWS Cloud Quest: Cloud Practitioner](https://skillbuilder.aws/learn/FU5WCYVGKY/aws-cloud-quest-cloud-practitioner/JF9TKU68GT)
    - [AWS Concepts (DataCamp)](https://www.datacamp.com/courses/aws-concepts)
    - [AWS Cloud Technology and Services (DataCamp)](https://www.datacamp.com/courses/aws-cloud-technology-and-services)
    - [Learning AWS from Scratch in 2025 (Video)](https://www.youtube.com/watch?v=0WVXTRMKXtE)
- **Related Lab**: [Lab 1: Cloud Concepts & CLI](labs/01-IAM_CLI.md)

---

## Module 2: Virtual Private Cloud (VPC)
*Designing your own private network in the cloud.*

- **Objectives**: Understand subnets, route tables, IGWs, and NAT Gateways.
- **Resources**:
    - [AWS Networking Basics For Programmers (Video)](https://www.youtube.com/watch?v=2doSoMN2xvI)
    - [Amazon VPC Basics Tutorial (Video)](https://www.youtube.com/watch?v=7_NNlnH7sAg)
    - [AWS VPC Beginner to Pro (FreeCodeCamp)](https://www.youtube.com/watch?v=g2JOHLHh4rI)
    - [Networking Core](https://skillbuilder.aws/learning-plan/KG2Z8NEHYV/networking-core--knowledge-badge-readiness-path-includes-labs/ZDTDSRZ9NE)
    - [How IP Addressing Works in AWS (Video)](https://www.youtube.com/watch?v=kRDtwr1dPpw)
    - [Internet Gateway VS NAT Gateway (Article)](https://aws.plainenglish.io/internet-gateway-vs-nat-gateway-a82c79958027)
- **Related Lab**: [Lab 2: Virtual Networking (VPC)](labs/02-VPC_Networking.md)

---

## Module 3: Compute & Storage
*Launching servers and managing data.*

- **Objectives**: Deploy EC2 instances and use S3 for object storage.
- **Resources**:
    - [Amazon EC2 Basics Tutorial (Video)](https://www.youtube.com/watch?v=hAk-7ImN6iM)
    - [Amazon S3 Basics Tutorial (Video)](https://www.youtube.com/watch?v=mDRoyPFJvlU)
- **Related Lab**: [Lab 3: Compute & Storage](labs/03-EC2_S3.md)

---

## Module 4: High Availability & Scaling
*Building systems that can handle traffic and recover from failure.*

- **Objectives**: Configure Load Balancers (ALB) and Auto Scaling Groups (ASG).
- **Resources**:
    - [Create an Application Load Balancer (Video)](https://www.youtube.com/watch?v=ZGGpEwThhrM)
    - [Route Traffic using Load Balancer Listener Rules (Video)](https://www.youtube.com/watch?v=0XMsnAgHXoo)
- **Related Lab**: [Lab 4: High Availability (ALB/ASG)](labs/04-ALB_ASG_Manual.md)

---

## Module 5: Security & DNS
*Securing your infrastructure and managing domain names.*

- **Objectives**: Master Security Groups vs NACLs and Route 53 DNS records.
- **Resources**:
    - [Domain Name System (DNS) Basics (Video)](https://www.youtube.com/watch?v=1cS2Nx7sxOM)
    - [Amazon Route 53 Basics Tutorial (Video)](https://www.youtube.com/watch?v=JRZiQFVWpi8)
    - [What Are NACLs in AWS? (Video)](https://www.youtube.com/watch?v=t4ZUhxBmVJM)
    - [AWS Security Groups Simply Explained (Video)](https://www.youtube.com/watch?v=uYDT2SsHImQ)
    - [Security Groups vs. NACLs: What’s the Difference? (Video)](https://www.youtube.com/watch?v=JWoNu2Mtpdg)
- **Related Lab**: [Lab 5: Advanced Networking & Security](labs/05-Advanced_EC2_VPC.md)

---

## Module 6: Infrastructure as Code (Terraform & Terragrunt)
*Automating the entire stack professionally.*

- **Objectives**: Master Terraform HCL, state management, and the Terragrunt DRY wrapper.
- **Resources**:
    - [Terraform in 10 Minutes (Video)](https://www.youtube.com/watch?v=tomUWcQ0P3k)
    - [Terraform Crash Course (Video)](https://www.youtube.com/watch?v=HmxkYNv1ksg)
    - [Why Terragrunt? (Article)](https://blog.gruntwork.io/terragrunt-vs-terraform-why-use-terragrunt-e4483c66288c)
    - [Terragrunt Quick Start Guide (Docs)](https://terragrunt.gruntwork.io/docs/getting-started/quick-start/)
- **Related Labs**:
    - [Lab 6: Intro to Terraform](labs/06-Intro_Terraform.md)
    - [Lab 7: Terraform Modules & Logic](labs/07-Terraform_Modules.md)
    - [Lab 8: Remote State & Data](labs/08-Remote_State.md)
    - [Lab 9: Intro to Terragrunt](labs/09-Intro_Terragrunt.md)
    - [Lab 10: Advanced Terragrunt](labs/10-Advanced_Terragrunt.md)

---

## 👨‍🏫 Mentor Guides
Answer keys and mentor-specific instructions can be found in `guides/mentor/`.

---

## 💰 Cost Management
**IMPORTANT**: In the Pluralsight Sandbox, resources are automatically deleted after 4 hours. Special care should be taken with NAT Gateways as they incur hourly costs.
