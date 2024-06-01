 <!-- markdownlint-disable-next-line -->
[![Image Hub](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/ysfaltun/projectx/general)  

# Minikube Cluster Setup with Terraform

## Overview
This project demonstrates how to set up a Minikube cluster using Terraform on Ubuntu. The setup includes installing essential tools, configuring the environment, and deploying a Minikube cluster with various addons.

## Prerequisites
Before proceeding, ensure you have the following:

- Ubuntu system
- Administrative access (sudo)
- Internet connection
- Kubernetes 1.23+
- Helm 3.8.0+
- Docker
- Access to a private Dockerhub Registry 
- Sops (optional) it was minikube because of that i didn't use

## Project Structure
The project includes the following main components:
- `enviroment-setup.sh`: A script to set up the environment by installing necessary tools and dependencies.
- `main.tf`: The Terraform configuration file to create the Minikube cluster.

## Environment Setup
Before running the Terraform configuration, you need to set up the environment by installing necessary tools such as Git, Java, Maven, Terraform, Helm, Docker, and Kubectl.
chmod +x enviroment_setup.sh
sudo ./enviroment_setup.sh

 ```
terraform init
terraform apply
 ```

After installation arrange config path.

 ```
export KUBECONFIG=/home/neox/Documents/.kube/config 
 ```
This README includes all necessary steps and explanations for setting up the environment and deploying the Minikube cluster using Terraform on an Ubuntu system.

I use this source:
https://registry.terraform.io/providers/scott-the-programmer/minikube/latest/docs
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any inquiries or issues, please contact your-email@example.com.
