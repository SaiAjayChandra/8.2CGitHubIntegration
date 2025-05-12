# 8.2C GitHub Integration with Jenkins

This project demonstrates the integration of GitHub with Jenkins using a Declarative Pipeline. It includes seven key stages that represent a standard CI/CD workflow for a Java-based project.

##  Jenkins Pipeline Stages

The Jenkinsfile in this repository defines the following stages:

1. **Build**
   - Builds the application using **Maven**.

2. **Unit and Integration Tests**
   - Executes tests using **JUnit** and **Postman**.

3. **Code Analysis**
   - Performs static code analysis using **SonarQube**.

4. **Security Scan**
   - Scans the project for vulnerabilities using **Snyk** or **OWASP Dependency-Check**.

5. **Deploy to Staging**
   - Deploys the application to a **staging environment on AWS EC2**.

6. **Integration Tests on Staging**
   - Runs integration tests in the staging environment.

7. **Deploy to Production**
   - Deploys the application to the **production environment on AWS EC2**.

## Technologies Used

- GitHub
- Jenkins
- Maven
- JUnit
- Postman
- SonarQube
- Snyk / OWASP Dependency-Check
- AWS EC2

##  Repository Contents

- `Jenkinsfile`: Defines the CI/CD pipeline stages.
- `README.md`: Project overview and pipeline documentation.

## Jenkins Integration

This repository is linked to a Jenkins pipeline that:
- Pulls the Jenkinsfile via SCM.
- Polls for changes in the GitHub repository.
- Automatically triggers builds upon updates.

## Author

**Sai Ajay Chandra Jagarlamudi**
