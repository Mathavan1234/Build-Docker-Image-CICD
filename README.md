# 🚀 CodeBuild CI/CD Project using Terraform & Docker

This project demonstrates a complete CI/CD pipeline using **AWS CodeBuild**, **Terraform**, and **Docker**. It consists of two main sections:

1. Deploying a static website hosted on an **EC2 instance** using Terraform.
2. Building and pushing a **Docker image** to **Docker Hub** using CodeBuild.

---

## 📁 Section 1: Deploy Static Website using CodeBuild & Terraform

### Overview
- Automate the deployment of a static website hosted on an EC2 instance.
- The pipeline is triggered whenever a new commit is pushed to the GitHub repo.

### Steps

1. **Create IAM User for CodeBuild**
   - Full admin access.
   - Generate AWS CLI credentials (Access Key + Secret).

2. **Terraform Script**
   - Write infrastructure as code to provision the EC2 instance.

3. **Shell Scripts**
   - `install-terraform.sh`: Installs Terraform.
   - `apply-terraform.sh`: Applies the Terraform configuration.
   - `configure-named-profile.sh`: Sets up AWS CLI named profile.

4. **Buildspec**
   - `buildspec.yml`: Defines CodeBuild phases (install, build, post_build).

5. **Create CodeBuild Project**
   - Link GitHub repo with a Personal Access Token (PAT).
   - Add environment variables: AWS credentials, region, profile.
   - On push, CodeBuild runs the Terraform script and provisions the EC2 instance.

---

## 🐳 Section 2: Build & Push Docker Image to Docker Hub

### Overview
- Create and push Docker images automatically via CodeBuild.

### Steps

1. **Create DockerHub Repository**

2. **Dockerfile**
   - Defines the application image.

3. **Shell Scripts**
   - `build-image.sh`: Builds the Docker image.
   - `push-image.sh`: Pushes the image to Docker Hub.

4. **Buildspec**
   - `buildspec.yml`: Executes Docker commands via CodeBuild.

5. **Create CodeBuild Project**
   - Connect GitHub repo.
   - Set environment variables: DockerHub credentials, repo name, image tag.
   - On commit, build and push Docker image to DockerHub.

---

## ✅ Project Status

- ✅ EC2 Instance is running and hosting the static website.
- ✅ Docker image successfully built and pushed to DockerHub.

---
