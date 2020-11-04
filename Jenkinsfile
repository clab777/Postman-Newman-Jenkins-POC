pipeline {
    agent { docker { image 'node:8.12.0' } }
    environment {
        HOME = '.'
    }
    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/clab777/Postman-Newman-Jenkins-POC.git'
            }
        }
        stage('Package Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm api-tests-prod'
            }
        }
    }
}
