# DevOps Engineer - Princeps Interview Assessment

This repository houses the codebase to PHP lavarel application to access the Terraform code for the infrastructure on AWS, hit this link; https://github.com/ibukun-oyedeji/Infrastrucuture.

# Infrastructure Overview
- **VPC**: A custom VPC in which the resource will be deployed into
- **Subnets**: Two public and two private
- **ASG**: Auto Scaling Group (ASG) configured to launch EC2 instances within the
subnets.
- **Application Load Balancer**: Load Balancer (ELB or ALB) to distribute traffic across the Instance hosts.
- **Ec2 Instances**: Ec2 instances running the PHP application.
- **RDS**: MySQL RDS Instance for Database.
- **Cloudwatch**: Cloud watch is configured for metrics monitoring.
- **ACM**: AWS Certificate Manager for serving certificate to the domain.
- **Route53**: The Route 53 for mapping records to the domain and also purchasing the domain.
- **Security Group**: Security for controlling inbound and outbound traffic.
-**SQS**: AWS Native Queue Service for distributed system.

## Deployment

We use the user-data.sh is used to clone the repo and start the application on the instances, triggered by pushes to the master branch. It handles:


## How To Deploy The Infrastructure?

To deploy the infrastructure, follow these steps:

- Navigate to the terraform repo on https://github.com/ibukun-oyedeji/Infrastrucuture and running `cd Infrastructure` in your terminal.
- Execute the command `terraform apply -auto-approve` to initiate the deployment process. This command automates the approval of the deployment, streamlining the process.

After the Terraform process completes, the URL; ibkaay.net for the load balancer will be displayed in the terminal. Copy and paste this URL into your browser to access the application.
