## What This Project Includes
- One VPC
- One Public Subnet
- One Private Subnet
- Bastion Host (EC2 in public subnet)
- Private EC2 Instance (no public IP)
- Internet Gateway for public subnet
- NAT Gateway for private subnet
- Route tables for public and private traffic
- Security groups for secure access

## How It Works (Simple Explanation)

# Public Subnet
- Contains the Bastion Host
- Has internet access through Internet Gateway

# Private Subnet
- Contains your main EC2 instance
- No direct internet access
- Uses NAT Gateway (in public subnet) to reach the internet

# Bastion Host
- You first SSH into the Bastion Host
- From Bastion, you connect to the private EC2 instance

# Security Groups
- Bastion allows SSH from your IP
- Private EC2 allows SSH only from Bastion

## Why This Project Is Useful
- Shows basic AWS networking
- Helps understand public vs private subnets
- Helps you learn routing and NAT
- Used in real cloud environments
