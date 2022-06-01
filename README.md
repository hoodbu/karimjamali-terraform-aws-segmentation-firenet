# Summary

This repository builds out a completed representation of the infrastructure created for the Aviatrix ACE Cloud Operations course.

It builds the following:

Aviatrix Transit with FireNet having Palo Alto Networks VM-series Firewalls.   
Another Aviatrix Transit without FireNet.   
2 Spoke VPCs (Prod/Dev) attached to Aviatrix Transit with FireNet.   
1 Spoke VPC (Shared Services) attached to the other Aviatrix Transit (Without Firenet).  
Aviatrix Transit in Azure with 2 spokes.   
Aviatrix Transit in GCP with 1 spoke.   
3 x Ubuntu VMs with Key Pairs where each Ubuntu VM lies in one spoke.    
Site2Cloud connection between AWS Transit with FireNet and on-prem (emulated by CSR in AWS).     

The general objective was to showcase Multi-Cloud Network Segmentation (MCNS) and FireNet. 

Component	Version
Aviatrix Controller	UserConnect-6.7.1186
Aviatrix Terraform Provider	> 2.21.2
Terraform	> 1.0
AWS Terraform Provider	> 3.0

Dependencies
Software version requirements met
Aviatrix Controller with Access Accounts defined for AWS, and GCP. Default account names are 'aws-account' and 'gcp-account' respectively.
Sufficient limits in place for CSPs and regions in scope (EIPs, Compute quotas, etc.)
Active subscriptions for the NGFW firewall images in scope
Terraform 1.0 in the user environment
Terraform provider requirements are met (AWS, GCP, Azure) in the runtime environment
Account credentials for each CSP defined in environment. The following environment variables will be needed:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
TF_VAR_azure_tenant_id
TF_VAR_azure_subscription_id
TF_VAR_azure_client_id
TF_VAR_azure_client_secret
GOOGLE_CREDENTIALS
Workflow
Modify terraform.tfvars as needed
terraform init
terraform plan
terraform apply

![Lab Setup - Page 8 (9)](https://user-images.githubusercontent.com/16576150/171320244-84c8af17-88f6-491f-b304-a6c58ce2413f.png)
