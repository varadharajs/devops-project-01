# 🚀 CI/CD Pipeline Automation using Jenkins and Docker

## 📌 Project Overview

This project demonstrates a basic CI/CD pipeline for automatically building and deploying a containerized web application.

Whenever code is pushed to GitHub, a GitHub Webhook automatically triggers Jenkins. Jenkins builds a Docker image and deploys the updated application on an AWS EC2 instance.

## 🏗️ Architecture

```text
Developer
    │
    │ git push
    ▼
GitHub Repository
    │
    │ GitHub Webhook
    ▼
Jenkins
    │
    │ Build Docker Image
    ▼
Docker Container
    │
    │ Deploy
    ▼
AWS EC2
    │
    ▼
Web Application
