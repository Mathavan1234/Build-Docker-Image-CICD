# 🚀 CodeBuild CI/CD Project using Terraform & Docker

This project demonstrates a complete CI/CD pipeline using **AWS CodeBuild**, **Terraform**, and **Docker**. 

Building and pushing a **Docker image** to **Docker Hub** using CodeBuild.

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

- ✅ Docker image successfully built and pushed to DockerHub.

---
