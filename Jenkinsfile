pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                bat 'mvn test'
                bat 'mvn verify'
            }
        }
        stage('Code Analysis') {
            steps {
                bat 'mvn sonar:sonar'
            }
        }
        stage('Security Scan') {
            steps {
                bat 'mvn org.owasp:dependency-check-maven:check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to AWS EC2 staging environment'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests in staging'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to AWS EC2 production environment'
            }
        }
    }
}

                
