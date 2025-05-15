# IAC with Terraform – Provisioning Docker Container on EC2

This task demonstrates how to provision an NGINX Docker container on an AWS EC2 instance using Terraform, following Infrastructure as Code (IaC) best practices.

## Tools Used

- Terraform  
- Docker  
- AWS EC2 (Ubuntu)  
- Git & GitHub  

## Objective

Provision a local NGINX web server inside a Docker container using Terraform. Verify it through a web browser and manage the full lifecycle using Terraform commands.

## Project Structure

- main.tf – Terraform configuration file to pull the NGINX Docker image and run a container  
- screenshots/ – Contains step-by-step execution screenshots  
- README.md – Documentation of the setup process  

## Setup Process (Step-by-Step)

### 1. Launch EC2
- Create and connect to an EC2 Ubuntu instance using SSH.

### 2. Install Docker and Terraform
- Install Docker to run containers.
- Install Terraform to manage the infrastructure.

### 3. Clone GitHub Repository
- Clone this GitHub repository onto the EC2 instance.

### 4. Initialize Terraform
- Run `terraform init` to initialize the Terraform project.

### 5. Plan the Deployment
- Run `terraform plan` to preview the infrastructure changes.

### 6. Apply the Configuration
- Run `terraform apply` to pull the NGINX image and start a container exposing it on port 8080.

### 7. Verify NGINX Web Server
- Use `docker ps` to ensure the container is running.
- Visit `http:16.16.173.170:8080` in a browser to view the default NGINX welcome page.

### 8. Check Terraform State
- Use `terraform state list` and `terraform state show` to inspect the tracked Docker resources.

### 9. Destroy the Infrastructure
- Run `terraform destroy` to clean up and remove the container and related resources.

## Screenshots

All screenshots related to the task have been uploaded individually as .png files in the main repository directory:

- Terraform initialization
- Terraform planning
- Terraform apply output
- Terraform state list output
- Browser view of the NGINX welcome page
- Terraform destroy output

## Outcome

- Successfully provisioned and verified an NGINX Docker container using Terraform  
- Demonstrated end-to-end lifecycle: init → plan → apply → verify → destroy  
- Managed infrastructure as code with Terraform
