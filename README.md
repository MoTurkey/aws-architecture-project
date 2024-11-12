# aws-architecture-project
Demo project for AWS architecture using CloudFormation and S3

## Project Overview
This project demonstrates an AWS cloud architecture setup using [S3, EC2& CloudFormation]. The goal of this project is to [briefly describe the purpose, like automate infrastructure deployment].

## Architecture Diagram
![AWS Architecture](https://github.com/user-attachments/assets/7ac996aa-a1ee-4423-80a5-d7795f8ee726)


## Project Components

## Code and Configuration

### CloudFormation Template
This project includes a CloudFormation template (`template.yaml`) that automates the setup of an S3 bucket and an EC2 instance.

- **S3 Bucket**: Creates an Amazon S3 bucket for storage.
- **EC2 Instance**: Deploys an Amazon EC2 instance with a specified key pair for SSH access.

To deploy this template:
1. Download the `template.yaml` file.
2. Go to the AWS Console, open the **CloudFormation** service, and create a new stack.
3. Upload `template.yaml` and follow the prompts to deploy the resources.

### S3 Bucket
This project includes an Amazon S3 bucket that serves as a foundational component for storing data and assets. Below are the setup details:

1. **Bucket Name**: `my-demo-bucket-mo`
2. **Region**: [e.g., `us-east-1`]
3. **Purpose**: This bucket will [e.g., host a static website].

To create this S3 bucket:
- Go to the **AWS Console** > **S3** service.
- Click **Create bucket** and enter the required details.
- Choose your region and leave the other settings as default.
- 
### EC2 Instance
This project includes an Amazon EC2 instance that provides [e.g., compute resources for a web server].

1. **Instance Name**: `demo-ec2-instance`
2. **AMI**: Amazon Linux 2 (or the OS you chose)
3. **Instance Type**: `t2.micro` (suitable for testing and free tier eligible)
4. **Key Pair**: [Key pair name used for SSH access]

**Setup Instructions**:
- Go to **AWS Console** > **EC2** service and click **Launch Instance**.
- Choose the `t2.micro` instance type and Amazon Linux 2 AMI.
- Select (or create) a key pair and configure other settings as needed.
- Launch the instance.

**Accessing the Instance**:
Use the public IP address assigned to the instance and the key pair to SSH into it:
```bash
ssh -i "your-key-pair.pem" ec2-user@[instance-public-ip]
