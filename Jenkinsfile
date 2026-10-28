pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-config:latest .'
            }
        }

        stage('Test Docker Image') {
            steps {
                sh 'docker image inspect devops-config:latest'
            }
        }
    }
}
