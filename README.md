# Automated Container Build & Delivery Pipeline (CI/CD)

[![Build and Push Docker Image](https://github.com/anaghagore07-bit/my-devops-pipeline/actions/workflows/ci.yml/badge.svg)](https://github.com/anaghagore07-bit/my-devops-pipeline/actions/workflows/ci.yml)
An automated continuous integration pipeline built using **GitHub Actions**, **Docker**, and **Docker Hub** to streamline container packaging and distribution.

## 🚀 Architecture & Workflow
1. **Source Trigger**: Developers push code or documentation updates to the `main` branch.
2. **Automated CI Runner**: GitHub Actions triggers an Ubuntu runner to checkout the codebase.
3. **Environment Setup**: Configures Docker Buildx builder instance for optimized multi-platform builds.
4. **Secure Authentication**: Authenticates with Docker Hub registry using encrypted repository secrets.
5. **Container Packaging**: Builds a lightweight production Nginx container (`alpine` base).
6. **Registry Distribution**: Pushes tagged release (`anaghagore/devops-demo-app:latest`) to Docker Hub.

## 🛠️ Tech Stack
* **Containerization**: Docker, Alpine Linux
* **CI/CD Automation**: GitHub Actions
* **Container Registry**: Docker Hub
* **Web Server**: Nginx

## 🏃 Run the Application Locally
Pull and run the latest image directly from Docker Hub:

```bash
docker run -d -p 8080:80 anaghagore/devops-demo-app:latest
