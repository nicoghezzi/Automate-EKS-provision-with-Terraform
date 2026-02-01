## Project Summary

Built and automated AWS infrastructure using Terraform, covering both foundational cloud networking and Kubernetes cluster provisioning. The project started with designing a modular VPC that included dynamic subnets, NAT gateways, and Kubernetes-aware tagging, followed by automated EC2 provisioning with Docker and NGINX to validate network isolation and bootstrap workflows.

The work then expanded into provisioning a production-ready Amazon EKS cluster using Terraform modules, integrating it with the existing VPC and deploying managed node groups in private subnets for security and scalability. The repository contains two branches, with the more advanced Kubernetes and EKS implementation available in the feature/eks branch.

## Tools Used

- Terraform
Used as the primary Infrastructure as Code tool to define modular AWS networking, EC2 resources, and EKS clusters.

- AWS (VPC, EC2, NAT Gateway, EKS, IAM): Provisioned cloud networking, compute, and managed Kubernetes services with secure defaults and private networking.

- Terraform AWS EKS Module: Leveraged to automate control plane creation and managed node group provisioning.

- Bash: Used for EC2 bootstrap scripting to install and configure Docker and NGINX during instance initialization.

## Skills I applied

- Terraform Module Design
Designed reusable and parameterized modules to support scalable VPC, EC2, and EKS infrastructure.

- AWS Cloud Networking
Configured VPCs with public and private subnets, NAT gateways, and DNS settings to support both EC2 workloads and private EKS node groups.

- Kubernetes Infrastructure Automation
Provisioned Amazon EKS clusters and managed node groups using Terraform, aligning Kubernetes workloads with AWS networking and IAM requirements.

- Infrastructure Orchestration
Gained hands-on experience with how Terraform coordinates AWS APIs and CloudFormation stacks during EKS provisioning.

## Some of the Challenges I faced

- Dynamic Availability Zone Management
Avoided hardcoded configurations by dynamically querying availability zones to improve portability and resilience.

- Private Subnet Connectivity
Enabled outbound internet access for private resources by correctly configuring NAT gateways and VPC DNS settings.

- EKS IAM and Node Group Setup
Automated IAM role creation and permissions required for EKS control plane and worker nodes, resolving common cluster bootstrap issues.

## Practical Experience

This project reflects real-world infrastructure work where cloud networking, compute, and Kubernetes must be designed together. It demonstrates the ability to build AWS environments from the ground up using Terraform, then layer a production-ready EKS cluster on top using modular, repeatable patterns. The separation into branches highlights an iterative approach, with the feature/eks branch showcasing the more advanced Kubernetes-focused implementation that a hiring manager can review in depth.