pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                sh '''
                python -m pip install --upgrade pip
                pip install --user -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                python app.py
                '''
            }
        }

    }
}