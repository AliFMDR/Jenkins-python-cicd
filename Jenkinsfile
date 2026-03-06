pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                sh '''
                python3 --version || python --version
                '''
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                pip3 install -r requirements.txt || true
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                nohup python3 app/app.py &
                '''
            }
        }

    }
}