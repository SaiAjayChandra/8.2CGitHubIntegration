# CI/CD Pipeline using Jenkins – Task 8.2C

## Overview

This project is created for **Task 8.2C** as part of the unit requirements. The task involves setting up a Jenkins pipeline that connects to a GitHub repository and simulates a CI/CD process using 7 defined stages. Each stage represents a key part of the software development lifecycle and uses a specific tool as required in the instructions.

This is a **theoretical design**, so instead of running actual commands, each stage prints a message (using `echo`) to represent the tool and action being performed. The Jenkins job is triggered by polling GitHub at regular intervals (no webhook is used).

## Repository Contents

- `Jenkinsfile` – Contains the declarative Jenkins pipeline.
- `README.md` – This file explaining the purpose and structure of the pipeline.

---

## Jenkins Pipeline Stages

The Jenkins pipeline includes the following 7 stages:

### 1. **Build**
- **Task:** Compiles and packages the source code.
- **Tool Used:** Maven

### 2. **Unit and Integration Tests**
- **Task:** Runs unit and integration tests to make sure the code works and components integrate.
- **Tool Used:** JUnit

### 3. **Code Analysis**
- **Task:** Analyzes the code quality and checks for bugs or bad practices.
- **Tool Used:** SonarQube

### 4. **Security Scan**
- **Task:** Scans for known security vulnerabilities in dependencies.
- **Tool Used:** OWASP Dependency-Check

### 5. **Deploy to Staging**
- **Task:** Simulates deployment to a staging server.
- **Tool Used:** Ansible

### 6. **Integration Tests on Staging**
- **Task:** Runs integration/API tests on the staging environment.
- **Tool Used:** Postman (via Newman CLI)

### 7. **Deploy to Production**
- **Task:** Simulates final deployment to the production server.
- **Tool Used:** Ansible

---

## Jenkins Job Setup

- A GitHub repository was created and connected to Jenkins.
- The pipeline job was set up to **poll SCM** for changes at regular intervals (no webhook used).
- The job runs the `Jenkinsfile` stored in the `main` branch of the repository.

This Jenkins pipeline successfully represents all the required stages with appropriate tools. Though no actual deployments or tests are performed, the structure reflects a real-world CI/CD pipeline using industry-standard tools.

---

**Author**  
Sai Ajay Chandra Jagarlamudi  
Student ID: *224646369*  
Deakin University – SIT223/SIT753  

