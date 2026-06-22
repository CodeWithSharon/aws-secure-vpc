# AWS Secure VPC Architecture

Multi-tier VPC with public and private subnets, bastion host access control.

## Architecture
Internet → IGW → Public Subnet (Bastion) → Private Subnet (App Server)

## Services Used
- Amazon VPC (10.0.0.0/16)
- EC2 (t3.micro)
- Security Groups (least privilege)
- Internet Gateway
- Public & Private Subnets

## Security Design
- Bastion host: SSH allowed only from my IP
- App server: SSH allowed only from bastion-sg
- App server has no public IP — completely private

## Resume Bullet
Designed and deployed a secure multi-tier AWS VPC with public subnet (bastion host) and private subnet (app server), configured Security Groups with least-privilege access and network segmentation.
