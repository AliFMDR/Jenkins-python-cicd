pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/AliFMDR/Jenkins-python-cicd.git'
            }
        }

        stage('Check Python') {
            steps {
                sh 'python --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Run App') {
            steps {
                sh 'python app/app.py'
            }
        }

    }
}