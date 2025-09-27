Terraform Project: VPC & AWS Infrastructure from Scratch

This repository demonstrates how to build AWS infrastructure from scratch using Terraform (HCL), including VPC, subnets, route tables, IGW (Internet Gateway), EC2 instances, load balancer, S3, and more.

📂 Repository Structure
File / Directory	Purpose
main.tf	Core resource definitions (VPC, subnets, routing, EC2, ALB, etc.)
provider.tf	AWS provider configuration & region settings
variables.tf	Input variables for infrastructure (CIDRs, instance types, etc.)
userdata1.sh	User data script to configure Apache on EC2 instance 1
userdata2.sh	User data script to configure Apache on EC2 instance 2
install.md	Steps to install and set up Terraform environment
aws-connection.md	Guide on AWS credentials, IAM setup, and connecting Terraform with AWS
README.md	This file — project overview and instructions
LICENSE	MIT license
🔍 Prerequisites

Before using this project, you should:

Have working knowledge of AWS services (VPC, EC2, subnets, route tables, IGW, load balancing, S3).

Install Terraform (v1.0+ recommended).

Configure AWS CLI or AWS credentials (Access Key, Secret Key, or IAM role with sufficient permissions).

🚀 Getting Started

Clone the repository:

git clone https://github.com/Faisal-sajid-Khan/Terrafrom_project_vpc_f-s-.git
cd Terrafrom_project_vpc_f-s-


Initialize Terraform:

terraform init


Review the Terraform plan:

terraform plan


Apply the Terraform configuration:

terraform apply


When prompted, type yes to confirm.

🛠️ What this project provisions

VPC with two public subnets across availability zones us-east-1a and us-east-1b.

Internet Gateway and Route Tables to route public traffic.

Security Group allowing inbound HTTP (port 80) and SSH (port 22) from anywhere.

Two EC2 Instances running Ubuntu, configured via userdata1.sh and userdata2.sh to install Apache and serve a simple HTML page.

An Application Load Balancer (ALB) that distributes incoming HTTP traffic between the two EC2 instances.

An S3 Bucket for storing files (bucket name: faisalterraform2024project).

📄 User Data Scripts

userdata1.sh and userdata2.sh install Apache HTTP Server, create a simple animated webpage displaying the instance ID, and enable the web server.

These scripts run on instance boot to automate web server setup.

🌐 Accessing the Application

After the Terraform apply completes successfully, you will get the ALB DNS name as output:

loadbalancerdns = <ALB_DNS_NAME>


Open this DNS URL in your browser to access the web application load balanced across your two EC2 instances.

⚠️ Important Notes

The EC2 instances use Ubuntu AMIs (ami-0360c520857e3138f for us-east-1a and ami-08982f1c5bf93d976 for us-east-1b). Change if needed.

Security Group allows SSH from anywhere (0.0.0.0/0), which is insecure for production—consider restricting SSH access.

Subnets are public and instances receive public IPs.

Ensure AWS credentials have sufficient permissions to create all required resources.

Modify CIDR blocks and regions in variables.tf or provider.tf as needed.

📚 References

Terraform AWS Provider Documentation

AWS VPC Documentation

Terraform User Data Documentation

🤝 Contributing

Feel free to fork, raise issues, or submit pull requests for improvements!

License

This project is licensed under the MIT License.

Created by Faisal Sajid Khan
