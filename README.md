Terraform Project Readme
This repository contains a Terraform project that automates the provisioning of infrastructure resources using the AWS provider. The project sets up a Virtual Private Cloud (VPC) with a subnet, an internet gateway, a route table, a security group, a network interface, an Elastic IP, and an EC2 instance running an Apache web server.

Prerequisites
Before running this Terraform project, ensure that you have the following prerequisites installed:

Terraform: You need to have Terraform installed on your local machine. You can download the latest version of Terraform from the official website: https://www.terraform.io/downloads.html. Make sure that the terraform command is available in your system's PATH.

AWS Account: You need to have an AWS account with appropriate permissions to create and manage resources like VPC, EC2 instances, etc.

Follow the steps below to run this Terraform project:

Clone the repository to your local machine:

--> git clone <repository_url>

Navigate to the project directory:

cd <project_directory>
Initialize the Terraform project by running the following command:

-- > terraform init
Review and customize the Terraform configuration:

Open the main.tf file and make any necessary changes to the configuration, such as the AWS region, CIDR blocks, availability zone, instance type, AMI, key name, etc. Ensure that the values are suitable for your environment.

Optionally, you can modify the user data script (user_data block in main.tf) to customize the setup of the EC2 instance.

Plan the execution of the Terraform project to see the planned changes:

--> terraform plan
Review the output to ensure that the planned changes match your expectations.

Apply the Terraform configuration to create the infrastructure:


--> terraform apply
Terraform will prompt for confirmation. Enter yes to proceed with the creation of resources.

Wait for Terraform to provision the infrastructure. The process may take a few minutes.

After the execution completes successfully, Terraform will display the outputs, including the public IP address of the EC2 instance.

Access the web server:

Open a web browser and enter the public IP address of the EC2 instance in the address bar. You should see the default Apache web page.

Cleanup (optional):

If you want to remove the created resources and destroy the infrastructure, you can use the following command:

--> terraform destroy

Terraform will prompt for confirmation. Enter yes to proceed with the destruction of resources.

Note: Be cautious when using the terraform destroy command as it will permanently delete the created resources and cannot be undone.

Conclusion
Congratulations! You have successfully set up and executed the Terraform project to automate the provisioning of AWS infrastructure resources. You can modify the configuration as needed and reuse this project to create and manage your infrastructure in a repeatable and version-controlled manner using Terraform.
