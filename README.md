# AWS EKS
## 📦 Demo 3
This project is part of **Module 11: Kubernetes on AWS (EKS)** in the **TWN DevOps Bootcamp**. The goal is to provision a fully managed Kubernetes cluster on **Amazon EKS** using the CLI tool `eksctl`, along with a **Node Group** for scalable compute resources.


## 📌 Objective
Use eksctl to automate the creation of:
- EKS cluster
- Manage EC2 NodeGroups

## 🚀 Technologies Used
- **Amazon EKS**: Amazon Elastic Kubernetes Service.
- **Amazon EC2**: Compute Instances used for worker nodes.
- **I AM**: AWS identity service to manage access and secure permissions.
- **kubectl**: CLI to interact with Kubernetes.
- **AWS CLI**: Interface for managing AWS services
- **CloudFormation**: To manage the VPC template.
- **eksctl**: CLI tool for creating and managing EKS clusters
  
## 📋 Prerequisites
- Ensure you have an AWS Account.
- Ensure AWS CLI is installed and configured.
- Kubectl is installed and configured to connect to the Kubernetes cluster.
  
## 🎯 Features
- Configure EKS cluster using eksctl

## 🏗 Project Architecture

<img src=""/>


## ⚙️ Project Configuration
### Install EKSCTL
1. Open the following link and follow the installation steps for your system.
   [Installing EKSCTL](https://eksctl.io/installation/)

 ### Create an EKS cluster using EKSCTL
 
1. Create an EKS cluster using eksctl
   ```bash
     eksctl create cluster \
     --name demo-cluster \
     --version 1.32 \
     --region us-east-2 \
     --nodegroup-name demo-nodes \
     --node-type t2.micro \
     --nodes 2 \
     --nodes-min 1 \
     --nodes-max 3
   ```
   <img src="https://github.com/lala-la-flaca/DevOpsBootcamp_11_AWS_EKS_eksctl/blob/main/Img/2%20cretaing%20cluster%20using%20eksctl.png" width=800 />
   
2. Verify nodes
   
   ```bash
   kubectl get nodes
   ```
   <img src="https://github.com/lala-la-flaca/DevOpsBootcamp_11_AWS_EKS_eksctl/blob/main/Img/3%20nodes%20created.png" width=800/>
