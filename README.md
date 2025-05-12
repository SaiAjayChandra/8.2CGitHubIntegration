# 8.2C GitHub Integration - Jenkins Pipeline Design

This repository is created for Task 1 of the DevSecOps module. It outlines a Jenkins pipeline with seven well-defined stages.

## Jenkins Pipeline Stages

### Stage 1: Build  
**Task:** Compile and package the application code.  
**Tool:** Maven

### Stage 2: Unit and Integration Tests  
**Task:** Run unit tests to verify code functionality and integration tests to ensure components work together.  
**Tools:** JUnit (for unit tests), TestNG (for integration tests)

### Stage 3: Code Analysis  
**Task:** Analyze the code to check for bugs, code smells, and adherence to coding standards.  
**Tool:** SonarQube

### Stage 4: Security Scan  
**Task:** Scan the code for known vulnerabilities in dependencies.  
**Tool:** Snyk

### Stage 5: Deploy to Staging  
**Task:** Deploy the built application to a staging environment for further testing.  
**Tool:** AWS CLI

### Stage 6: Integration Tests on Staging  
**Task:** Run integration tests in the staging environment to validate application behavior.  
**Tool:** Newman (Postman CLI)

### Stage 7: Deploy to Production  
**Task:** Deploy the verified application to the production environment.  
**Tool:** Jenkins (with SSH plugin or AWS CLI)
