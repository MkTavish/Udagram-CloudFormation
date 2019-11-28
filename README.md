#  Cloud Formation Template
## Creating an AWS infrastructure with Cloud Formation

https://github.com/MkTavish/Udagram-CloudFormation/blob/master/Web%20Architecture1.pdf

## **Prerequisites**
 - Create an AWS account.
 - Make sure you're signed into AWS as an IAM user with admin access. Do not sign in via the root account.
 - Create an EC2 key pair. 
 - Clone this repo so that you have a local copy of the templates.
 
## **Creating stacks**
Use the AWS CloudFormation Console to run the templates. Click the "Create Stack" button in the upper left corner of the console, then under "Choose a template", select "Upload a template to Amazon S3" and click "Browse" to find your local fork of this repository and choose this template to run.

Using the CLI. From your integrated Terminal, make sure you have the AWS CLI installed. Run "AWS Configure" to configure your terminal with the IAM user credentials you created earlier, then run `aws cloudformation create-stack --stack-name '_your stack name_' --region '_preferred region_' --template-body file://'_yaml file_' --parameters file://'_json parameter file_'`
Verify in the CloudFormation console that your stack has been created

## **This template creates**
 - A VPC
 - Public Subnet
 - Private Subnet
 - NAT Gateway
 - A Single EC2 Instance on Public Network with Public IP
 - Linux AMI
 - Launch Configuration
 - Autoscaling Group
 - Elastic Load Balancer
 - Create Proxy Access Security Group
 - EBS Volume
