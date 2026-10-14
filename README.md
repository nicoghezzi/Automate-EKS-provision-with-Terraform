# 🚀 AWS Infra & Kubernetes (Terraform + EKS)

![Infrastructure: Terraform](https://img.shields.io/badge/Infrastructure-Terraform-%235835CC?style=for-the-badge&logo=terraform&logoColor=white)
![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-%23FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes: EKS](https://img.shields.io/badge/Kubernetes-EKS-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Compute: EC2](https://img.shields.io/badge/Compute-EC2-%23FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white)
![Networking: VPC](https://img.shields.io/badge/Networking-VPC-%23232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

A production-style infrastructure project that demonstrates how to design and provision **scalable AWS cloud environments** using **Terraform**, evolving from foundational networking to a **fully automated Amazon EKS cluster** deployed in secure private subnets.

---

## 📌 Project Overview

This project showcases an end-to-end infrastructure journey:

- Designed a **modular VPC architecture** with dynamic subnets, NAT gateways, and Kubernetes-aware tagging  
- Provisioned **EC2 instances with Docker + NGINX** to validate networking and bootstrap workflows  
- Extended the platform to deploy a **production-ready Amazon EKS cluster** using Terraform modules  
- Implemented **managed node groups in private subnets** for improved security and scalability  
- Structured development using branches, with advanced implementation in `feature/eks`

---

## 🧰 Tech Stack

- **Terraform** – Infrastructure as Code for AWS resources and EKS provisioning  
- **AWS** – VPC, EC2, NAT Gateway, IAM, and EKS  
- **Terraform AWS EKS Module** – Simplified Kubernetes control plane and node group setup  
- **Bash** – EC2 bootstrap automation (Docker + NGINX setup)

---

## 🧪 Practical Experience

This project reflects real-world infrastructure engineering where **networking, compute, and Kubernetes must work together**.

- Built AWS infrastructure **from scratch using Terraform**
- Layered a **production-ready Kubernetes platform (EKS)** on top  
- Applied **modular, repeatable patterns used in real environments**
- Demonstrated **iterative development**, with:
  - Base infrastructure in `main`
  - Advanced Kubernetes implementation in `feature/eks`

---

## 🧠 Engineering Decisions & Trade-offs

| Decision | Rationale | Trade-off |
|---|---|---|
| **Terraform modules over custom resources** | Reused established patterns to provision VPC networking and EKS infrastructure consistently, reducing duplicated code and provisioning time. | Introduces module dependencies and requires version management and understanding of module defaults. |
| **Private subnets for EKS worker nodes** | Keeps worker nodes off direct public internet exposure while allowing required outbound connectivity through NAT gateways. | NAT gateways add hourly and data-processing costs; routing and connectivity require additional configuration. |
| **Managed node groups over self-managed nodes** | Delegates node provisioning and lifecycle integration to AWS, reducing operational overhead. | Provides less control over the underlying node lifecycle and requires understanding AWS-managed upgrade and scaling behavior. |
| **Dynamic Availability Zone discovery** | Avoids hardcoding Availability Zones, making the configuration more adaptable across supported regions. | Available zones and regional service capacity can differ, so subnet and resource assumptions still require validation. |
| **Layered infrastructure provisioning** | Built foundational VPC and EC2 networking first, then extended the architecture to EKS. This made dependencies easier to isolate and troubleshoot. | Adds intermediate configuration and requires careful management of dependencies and Terraform state. |

**Key outcome:** Automated end-to-end EKS infrastructure provisioning with Terraform modules, reducing provisioning time to under 20 minutes. The design prioritizes repeatability, private networking, and reduced operational overhead while making cost and complexity trade-offs explicit.

---

## 💡 Key Skills Demonstrated

### 🏗️ Terraform Module Design
- Built reusable and parameterized modules for VPC, EC2, and EKS  
- Enabled scalable and maintainable infrastructure patterns  

### 🌐 AWS Cloud Networking
- Configured **public/private subnets**, NAT gateways, and DNS  
- Supported secure communication for EC2 workloads and EKS nodes  

### ☸️ Kubernetes Infrastructure Automation
- Provisioned **Amazon EKS clusters and managed node groups**  
- Integrated Kubernetes with AWS IAM and networking  

### ⚙️ Infrastructure Orchestration
- Understood how Terraform interacts with AWS APIs and CloudFormation  
- Managed dependencies across networking and Kubernetes layers  

---

## ⚠️ Challenges & Solutions

### 🔄 Dynamic Availability Zones
- Avoided hardcoding by dynamically querying AZs  
- Improved portability and resilience across regions  

### 🔐 Private Subnet Connectivity
- Enabled outbound internet access via **NAT gateways**  
- Configured VPC DNS for proper service resolution  

### 🧩 EKS IAM & Node Group Setup
- Automated IAM roles and permissions for cluster + nodes  
- Resolved common bootstrap and access issues  

---

## 🚀 Author
Nicolas Ghezzi LinkedIn: https://www.linkedin.com/in/nghezzi/
