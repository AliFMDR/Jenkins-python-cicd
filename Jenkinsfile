pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/AliFMDR/Jenkins-python-cicd.git'
            }
        }

        stage('Install Python') {
            steps {
                sh '''
                apt update
                apt install -y python3 python3-pip
                '''
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                pip3 install -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                python3 app/app.py
                '''
            }
        }

    }
}