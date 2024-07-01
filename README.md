![image](https://github.com/Nithish14R/Devops-two-tier-python-app/assets/99314885/9937746d-736b-41bd-bfda-3943223913c5)


# How to setup two-tier application deployment on kubernetes cluster

# Two-Tier Python Application with MySQL on AWS EC2

This project demonstrates the deployment of a two-tier Python application with MySQL using AWS EC2 instances. The infrastructure includes a VPC with a public subnet for the frontend application and a private subnet for the MySQL database.

## Architecture

- **VPC**: Custom VPC with one public subnet and one private subnet.
- **Public Subnet**: Hosts the frontend Python application.
- **Private Subnet**: Hosts the MySQL database.
- **Security Groups**: Configured to allow communication between the frontend and the database.

## Prerequisites

- AWS Account
- AWS CLI installed and configured
- Python 3.x installed
- Git installed

## Setup
SSH into public VM

ssh ubuntu@x.x.x.x

### 1. Clone the Repository

```bash
**Install Kubernetes im installed kubernetes using microk8s**


1.Install MicroK8s
sudo snap install microk8s --classic --channel=1.30

2.Join the group
sudo usermod -a -G microk8s $USER
mkdir -p ~/.kube
chmod 0700 ~/.kube
su - $USER

3.Check the status
microk8s status --wait-ready

4.Access Kubernetes
microk8s kubectl get nodes

…or to see the running services:
microk8s kubectl get services

alias kubectl='microk8s kubectl'
microk8s kubectl get pods

5.Use add-ons
microk8s enable dns
microk8s enable hostpath-storage

6.Incase if any error in kubernetes:
microk8s stop
microk8s start

------------------------------------------------------------------

Install Docker on Ubunti
sudo apt install docker.io -y

git clone https://github.com/yourusername/your-repo.git
cd your-repo





