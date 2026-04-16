# 🚀 EKS Deployment using Terraform & Kubernetes

This project demonstrates an end-to-end DevOps workflow where AWS infrastructure is provisioned using Terraform and an application is deployed on Kubernetes (EKS).

---

## 📌 Project Overview

In this project, I have:

* Provisioned AWS infrastructure using Terraform
* Created a VPC with public and private subnets
* Deployed an EKS (Elastic Kubernetes Service) cluster
* Configured managed node groups (EC2 instances)
* Connected to the cluster using kubectl
* Deployed an Nginx application as a Pod
* Exposed the application using a LoadBalancer Service

---

## 🏗️ Architecture

```
Terraform
   ↓
AWS Infrastructure (VPC + Subnets + NAT Gateway)
   ↓
EKS Cluster (Control Plane)
   ↓
Worker Nodes (EC2 instances in private subnet)
   ↓
Pods (Nginx Application)
   ↓
Kubernetes Service (LoadBalancer)
   ↓
Public Access (Browser)
```

---

## 🛠️ Tech Stack

* Terraform (Infrastructure as Code)
* AWS (EKS, EC2, VPC, IAM)
* Kubernetes (kubectl)
* Docker (Nginx image)

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```
git clone https://github.com/<your-username>/eks-terraform-kubernetes-deployment.git
cd eks-terraform-kubernetes-deployment
```

### 2. Initialize Terraform

```
terraform init
```

### 3. Apply Infrastructure

```
terraform apply
```

### 4. Configure kubectl

```
aws eks update-kubeconfig --region us-east-1 --name demo-eks
```

### 5. Deploy Application

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 6. Access Application

```
kubectl get svc
```

Copy the LoadBalancer URL and open it in your browser.

---

## 📚 Key Learnings

* Understanding Kubernetes architecture (Control Plane vs Nodes)
* Role of kubelet, scheduler, and kubectl
* Importance of VPC and subnet design
* Why Pods are not directly accessible
* How Services and LoadBalancers expose applications

---

## 💡 Future Improvements

* Add Ingress Controller (NGINX / ALB)
* Implement CI/CD pipeline (GitHub Actions)
* Deploy multi-container applications
* Add monitoring (Prometheus + Grafana)

---

## 🤝 Acknowledgement

This project helped me gain hands-on experience with DevOps, Cloud Infrastructure, and Kubernetes fundamentals.

---

## ⭐ If you found this useful, consider giving it a star!
