# Terraform Project: VPC & AWS Infrastructure from Scratch

This repository demonstrates how to build AWS infrastructure from scratch using **Terraform (HCL)**, including VPC, subnets, route tables, IGW (Internet Gateway), EC2 instances, load balancer, S3, and more.

---

## 📂 Repository Structure

| File / Directory     | Purpose |
|----------------------|---------|
| `main.tf`            | Core resource definitions (VPC, subnets, routing, etc.) |
| `provider.tf`        | AWS provider configuration & region settings |
| `variables.tf`       | Input variables for the infrastructure (CIDRs, instance types, etc.) |
| `install.md`         | Steps to install and set up Terraform environment |
| `aws-connection.md`  | Guide on AWS credentials, IAM setup, and connecting Terraform with AWS |
| `README.md`          | This file — project overview and instructions |
| `LICENSE`            | MIT license |

---

## 🔍 Prerequisites

Before using this project, you should:

- Have working knowledge of AWS services (VPC, EC2, subnets, route tables, IGW, load balancing, S3) via console or CLI.
- Install **Terraform** on your workstation.  
- Configure AWS CLI / credentials (AWS Access Key, Secret Key, or IAM role).

---

## 🚀 Getting Started

Follow these steps to deploy the infrastructure:

1. Clone this repository:

   ```bash
   git clone https://github.com/Faisal-sajid-Khan/Terrafrom_project_vpc_f-s-.git
   cd Terrafrom_project_vpc_f-s-
