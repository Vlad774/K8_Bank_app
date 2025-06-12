# 🚀 EKS Kubernetes Deployment with Terraform, MySQL, and Spring Boot BankApp
##  📌 Description
This project demonstrates the deployment of a full-stack Spring Boot Banking Application and a MySQL database in a highly available and scalable Amazon EKS (Elastic Kubernetes Service) cluster using Terraform, Kubernetes manifests, and AWS native integrations. It follows modern DevOps practices, including Infrastructure as Code (IaC), secure secret handling, persistent storage with EBS, and dynamic service discovery.

## 🛠Technologies
- **Amazon EKS** → Managed Kubernetes cluster on AWS
- **Terraform** → Infrastructure provisioning and automation (IaC)
- **Kubernetes** → Container orchestration for scalable application management
- **AWS EBS CSI Driver** → Kubernetes cluster interaction & EKS utilities
- **kubectl & eksctl** → Cloud hosting for scalability
- **GitHub** → Source control and manifest hosting
  
## ⚙ Deployment Workflow
- 1️⃣ Infrastructure provisioning with Terraform to create EKS cluster, IAM roles, networking components (VPC, subnets, etc.)
- 2️⃣ Configuration of kubeconfig to connect to the new cluster using AWS CLI
- 3️⃣ Association of IAM OIDC provider to enable IAM roles for Kubernetes ServiceAccounts
- 4️⃣ Creation of an IAM ServiceAccount for the AWS EBS CSI Driver using eksctl
- 5️⃣ Installation of the EBS CSI Driver to dynamically provision persistent volumes
- 6️⃣ Deployment of MySQL with:
    Encrypted Secrets for credentials
    ConfigMap for DB initialization
    EBS-backed PersistentVolumeClaim
- 7️⃣ Deployment of Spring Boot BankApp, connected to the MySQL service
- 8️⃣ Exposure of BankApp via a LoadBalancer Service to enable external access
  
  
     
## ✨ Key Features
- ✔  Production-ready EKS setup using Terraform (IaC)
- ✔  Secure and modular deployment via Kubernetes manifests
- ✔  Persistent storage using AWS EBS and CSI driver
- ✔ Scalable architecture with cloud-native storage and external service exposure
- ✔ Load-balanced external access to Spring Boot BankApp using Kubernetes Service
  
## Walk-through:
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/Ec2.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/Ec2.png) 
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/volumes.png) 
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/running_services.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/running-nodes.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/manifest_deploy.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/Bank_running.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/Deleted_pod.png)
 ![First try](https://github.com/Vlad774/K8_Bank_app/blob/main/images/data_keeped_after_pod_deletion.png)
