# 🚀 AWS Infrastructure & Kubernetes Platform (Terraform + EKS)

![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-%23FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)  
![IaC: Terraform](https://img.shields.io/badge/IaC-Terraform-%235835CC?style=for-the-badge&logo=terraform&logoColor=white)  
![Kubernetes: EKS](https://img.shields.io/badge/Kubernetes-EKS-blue?style=for-the-badge&logo=kubernetes)  
![Compute: EC2](https://img.shields.io/badge/Compute-EC2-orange?style=for-the-badge&logo=amazon-ec2)  
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

## 🧪 Practical Experience

This project reflects real-world infrastructure engineering where **networking, compute, and Kubernetes must work together**.

- Built AWS infrastructure **from scratch using Terraform**
- Layered a **production-ready Kubernetes platform (EKS)** on top  
- Applied **modular, repeatable patterns used in real environments**
- Demonstrated **iterative development**, with:
  - Base infrastructure in `main`
  - Advanced Kubernetes implementation in `feature/eks`
