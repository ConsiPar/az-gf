 <!-- markdownlint-disable-next-line -->
[![Image Hub](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/ysfaltun/projectx/general)  

# ProjectX

## Overview
This project demonstrates how to set up a Minikube cluster using Terraform on Ubuntu. The setup includes installing essential tools, configuring the environment, and deploying a Minikube cluster with various addons.
After that we create RabbitMQ on that cluster via Helm and we integrate with two application.

##Steps
1- Local Git server installed for each part
![image](https://github.com/ada-url/ada/assets/8115505/05bd8cb1-90b1-44de-9899-c2c1baf9b38d)

2- Created folder structure
![image](https://github.com/ada-url/ada/assets/8115505/a838c136-d409-4674-ab6c-8a7572422579)

4- Craeted script for Ubuntiu setup  (projectx-infrastructure/..sh)
![image](https://github.com/ada-url/ada/assets/8115505/04532952-5290-4e32-a572-ee4fa26f709c)

3- Minikube created via terraform (projectx-infrastructure)
![image](https://github.com/ada-url/ada/assets/8115505/992ecf8f-f510-4f6c-9d09-cd384eaeb850)

4- RabbitMQ server created with Helm
![image](https://github.com/ada-url/ada/assets/8115505/8bd4ee6b-bc3e-4dfb-8ee8-c93b157ed49a)

5- Spring Java applications created (projectx-applications/xservices/consume or send service)
![image](https://github.com/ada-url/ada/assets/8115505/e95e00ab-02f2-4f93-98e0-3b6866bed165)

6- Docker images created - docker hub priveted registry used.

7- Helm chart created for apps (projectx-applications/xhelm - one chart multiple values file)

  
## Each module contains a README file that provides detailed steps and information about the module.
 
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

Results:
![consume](https://github.com/ada-url/ada/assets/8115505/c849f190-2531-4e21-995e-e480e7a2cab8)

![send](https://github.com/ada-url/ada/assets/8115505/8a930a99-129c-4d7b-8a48-65ed75cb4f77)


This README includes all necessary steps and explanations for setting up the environment and deploying the Minikube cluster using Terraform on an Ubuntu system.

I use this source:
https://registry.terraform.io/providers/scott-the-programmer/minikube/latest/docs
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any inquiries or issues, please contact your-email@example.com.
