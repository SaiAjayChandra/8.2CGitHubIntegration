pipeline {
    agent any  

    stages {
        
        stage('Build') {
            steps {
                echo 'Building the code using Maven'  
                bat 'mvn clean install'  
            }
        }

        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit'  
                bat 'mvn test'  

                echo 'Running integration tests using JUnit'  
                bat 'mvn verify'  
            }
        }

        
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis using SonarQube'  
                bat 'mvn sonar:sonar'  
            }
        }

        /
        stage('Security Scan') {
            steps {
                echo 'Running security scan using OWASP Dependency-Check'  
                bat 'dependency-check --scan .' 
            }
        }

       
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to AWS EC2 staging environment'  
               
            }
        }

        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests in staging environment'  
                bat 'mvn verify'  
            }
        }

        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to AWS EC2 production environment'  
                
            }
        }
    }
}
