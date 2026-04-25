Production-standard AWS infrastructure using Terraform.
- **IaC:** Terraform (modular, remote backend)
- **Cloud:** AWS (VPC, EC2, EKS)
- **State:** S3 + DynamoDB state locking
- **CI/CD:** Jenkins + ArgoCD
- **Orchestration:** Kubernetes (EKS)
## Structure
├── environments/     # dev and prod environments
├── modules/          # reusable Terraform modules
│   ├── vpc/
│   ├── ec2/
│   ├── eks/
│   ├── iam/
│   └── sg/
└── backend/          # S3 + DynamoDB backend config
## Environments
| Environment | State Backend | Region |
|---|---|---|
| dev | S3 + DynamoDB lock | ap-south-1 |
| prod | S3 + DynamoDB lock | ap-south-1 |
