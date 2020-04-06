## Week2

### Amazon Virtual Private Could (VPC)
VPC (10.0.0.0/16) 
- Subnet  (10.10.1.0/24) VPC <-> IGW <-> Subnet
  - EC2  
- Private Subnet (10.10.2.0/24)  
  - M  
- Subnet (10.10.3.0/24)  
  - EC2  
- Private Subnet (10.10.4.0/24)  
  - S 
  
EC2 <-> ELB <-> EC2  
Elastic Load Blancer (ELB)
 
 
 
### Amazon Storage 
Two kinds of storage:  
- Object storage: S3, Amazon Simple Storage Servie
- Block storage: RDS  

Elatic Block Storage (EBS) can attach to only one EC2 instance at a time. 

Amazon Elastic File System (EFS) can be attached to multiple EC2 instances simultaneously. 

