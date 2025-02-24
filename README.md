# 🚀 Jenkins CI/CD Pipeline for Node.js/React Application  

This repository contains a **Jenkins CI/CD pipeline** that automates the **building, testing, and deployment** of a **Node.js/React** application. The pipeline streamlines the development workflow by automating key stages in software delivery.  

---

## 📌 Features  

### ✅ **Continuous Integration & Deployment (CI/CD)**  
- Uses a **Jenkinsfile** to automate the **build, test, and deployment** process.  
- Implements **manual approval gates** before final deployment.  

### ✅ **Pipeline Stages**  
- **🔹 Checkout Code (SCM Checkout)** – Fetches the latest code from GitHub using SSH authentication.  
### 🔹 **1. Build Stage** – Installs dependencies
```sh
npm install
```

### 🔹 **2. Test Stage** – Runs application health checks
Since Jest is not used, this stage can include:
- **Linting checks** (optional)
- **Basic server response verification**

```sh
# Example: Check if Node.js server is running
curl -f http://localhost:3000/ || echo "Server is not responding"
```

### 🔹 **3. Deliver Stage (Deployment Step)**
**a) Builds the React app:**
```sh
npm run build
```
**b) Runs the application in the background:**
```sh
npm start &
```

### 🔹 **4. Manual Approval for Deployment**
- Ensures controlled releases before stopping the current running app.
- This step allows manual intervention before final deployment.

### 🔹 **5. Cleanup & Process Termination**
- Safely stops the currently running app before a new deployment:
```sh
kill $(cat .pidfile)
```

---

## 🚀 **Future Improvements**
- ✅ Integrate **unit tests** using Mocha or Jest (if required in the future).
- ✅ Automate **deployment to a cloud platform** (AWS, Azure, or GCP).
- ✅ Add **Docker support** for containerization.
- ✅ Implement **rollback strategy** in case of deployment failures.
