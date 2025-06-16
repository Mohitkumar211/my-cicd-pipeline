# CI/CD Pipeline with GitHub Actions, CircleCI, Jenkins & Docker

## 🚀 Project Overview

This project demonstrates how to set up a Continuous Integration and Continuous Deployment (CI/CD) pipeline using **GitHub Actions**, **CircleCI**, **Jenkins**, and **Docker**. It is aimed at helping beginners and students understand how modern DevOps pipelines work using different industry tools.

---

## 📌 What is CI/CD?

- **Continuous Integration (CI)**: Automatically builds and tests code changes to detect issues early.
- **Continuous Deployment (CD)**: Automatically deploys tested code to production or staging environments.

---

## 🧰 Tools & Technologies Used

| Tool         | Purpose                              |
|--------------|---------------------------------------|
| GitHub Actions | Automate builds/tests via GitHub    |
| CircleCI     | Cloud-based CI/CD automation          |
| Jenkins      | Self-hosted CI/CD pipeline server     |
| Docker       | Containerization of the application   |

---

## 🛠️ How the Pipelines Work

This project sets up **three CI/CD pipelines** using the same application and Docker image.

### ✅ GitHub Actions

- Triggers on `push` or `pull_request` to `main`
- Steps:
  - Checkout code
  - Build Docker image
  - Run tests
  - Push image to Docker Hub
  - (Optional) Deploy to server

**File:** `.github/workflows/main.yml`

---

### ✅ CircleCI

- Triggers on push to repository
- Steps:
  - Use Docker executor
  - Install dependencies & run tests
  - Build and push Docker image

**File:** `.circleci/config.yml`

---

### ✅ Jenkins

- Jenkins polls the GitHub repository or uses a webhook
- Steps:
  - Clone repo using Git plugin
  - Build and test application
  - Build Docker image
  - Push image to Docker Hub
  - Optional deployment step

**File:** `Jenkinsfile`

---

## 📁 Project Structure
![image](https://github.com/user-attachments/assets/71ec89d8-3b1e-4afd-ad9c-dadc83e65276)

---

## ✅ Prerequisites

- GitHub account
- Docker installed locally
- Docker Hub account
- CircleCI account (login via GitHub)
- Jenkins installed (locally or via VM)
- Basic understanding of YAML and Git

---

## ▶️ Running the Pipelines

### GitHub Actions
```bash
git push origin main

---

# Build Docker image
docker build -t your-app-name .

# Run container
docker run -p 3000:3000 your-app-name

# Push to Docker Hub
docker tag your-app-name yourdockerhubusername/your-app-name
docker push yourdockerhubusername/your-app-name






