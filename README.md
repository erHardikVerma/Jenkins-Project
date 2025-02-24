# 🚀 Jenkins CI/CD Pipeline for Node.js/React Application  

This repository contains a **Jenkins CI/CD pipeline** that automates the **building, testing, and deployment** of a **Node.js/React** application. The pipeline streamlines the development workflow by automating key stages in software delivery.  

---

## 📌 Features  

### ✅ **Continuous Integration & Deployment (CI/CD)**  
- Uses a **Jenkinsfile** to automate the **build, test, and deployment** process.  
- Implements **manual approval gates** before final deployment.  

### ✅ **Pipeline Stages**  
- **🔹 Checkout Code (SCM Checkout)** – Fetches the latest code from GitHub using SSH authentication.  
- **🔹 Build Stage** – Installs project dependencies using:  
  ```sh
  npm install
