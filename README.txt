Terry Welch: Project 2 - Udagram

URL: 
- This can be used to access the Udagram application running on the EC2 instances within my Private Subnets 


PROJECT NOTES:
I split the templates and paramaters into 2 files, one for the network components and the other for the server components.
As part of the launch configuration, the EC2 instances are assigned an S3 Read Only role via an Instance Profile. 
As part of the launch configuration, the EC2 instances will install AWS CLI and run a command to copy the website (index.html) from an S3 Bucket (my-603604765048-bucket).
When the udagram_servers.yml script is executed, I am exporting the Public URL for the Load Balancer as an Output 


Supporting Documentation:

01_Udagram_Solution_Architecture.png 
- VPC
- 2 Public Subnets (AZ1 + AZ2)
- 2 Private Subnets (AZ1 + AZ2)
- Internet Gateway
- NAT Gateways 
- Route Tables 

- Load Balancer 
- Autoscaling Group 
- EC2 Servers (2 in AZ1, 2 in AZ2)
- Load Balancer Security Group
- EC2 Security Group 



Parameters:




Outputs:




