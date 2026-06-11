# CloudFormation-template-vpc-s3-ec2
Using CloudFormation template created an EC2 instance , VPC  and S3 bucket 

CloudFormation is an Infrastructure as a Code (Iac) which is similiar as Terraform where it creates , updates and manages automatically AWS services.
with the help of scripts can create Cloudformation infrastructure and multiple resources.
CloudFormation makes it comfy, easy for on-premise/business to create multiple AWS servies. 

->  If any error occurred or the script (code) gets failed, the cloudformation Rollbacks the changes immediately and share error in Events section.

Here’s a simple AWS CloudFormation template that creates:

🌐 A VPC

🖥️ An EC2 instance

🪣 An S3 bucket

This template is beginner-friendly and uses YAML format.

📄 CloudFormation Template (YAML)
🛠️ How to Deploy This Template
1. Save the template

Save the above code as:

2. Upload via AWS Console

Go to AWS CloudFormation

Click Create stack

Choose Upload a template file

Select template.yaml

Provide the KeyPairName parameter (an existing EC2 key pair)

Click Create stack

3. Deploy via AWS CLI

Replace my-keypair with your existing EC2 key pair name.

📦 What This Template Creates

VPC: 10.0.0.0/16

Public Subnet: 10.0.1.0/24

Internet Gateway for internet access

Route Table with a default route to the internet

Security Group allowing SSH (port 22)

EC2 Instance (t2.micro, Amazon Linux 2)

S3 Bucket with versioning enabled

⚠️ Important Notes

The AMI ID ami-0c02fb55956c7d316 is valid for us-east-1. If you deploy in another region, update the AMI ID accordingly.

Ensure you have an existing EC2 Key Pair in the target region.

The S3 bucket name must be globally unique, so the template appends your AWS Account ID automatically.

🎯 Output Example

After deployment, CloudFormation will display outputs such as:

VPC ID

EC2 Instance ID

S3 Bucket Name

You can use these outputs for further automation or integration with other AWS services.
