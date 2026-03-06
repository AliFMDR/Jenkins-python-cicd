pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                sh '''
                which python || true
                which python3 || true
                '''
            }
        }

        stage('Run App') {
            steps {
                sh 'echo CI/CD Pipeline Success'
            }
        }

    }
}