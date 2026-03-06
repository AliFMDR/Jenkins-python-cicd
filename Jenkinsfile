pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-cicd-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 5000:5000 python-cicd-app'
            }
        }

    }
}