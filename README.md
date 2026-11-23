## Project Overview

This project provisions AWS VPC infrastructure using Terraform with a modular and reusable architecture. It uses a root module to configure the environment and a reusable VPC module to manage VPC resources.

GitLab CI/CD can be used to automate Terraform workflows.

## Project Structure

```text
your-gitlab-repo/
├── .gitlab-ci.yml           # GitLab CI/CD pipeline configuration
├── main.tf                 # Root configuration that calls the VPC module
├── variables.tf             # Input variables for your environment
├── outputs.tf               # Exposes module outputs (like VPC ID)
└── modules/
    └── vpc/
        ├── main.tf          # Reusable VPC resource definition
        ├── variables.tf     # Module input parameters
        └── outputs.tf       # Module return values
```