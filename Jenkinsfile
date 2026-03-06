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

        stage('Run App') {
            steps {
                sh 'python app/app.py'
            }
        }

    }
}