pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }

    environment {
        VENV_DIR = "venv"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh '''
                set -e
                python -m venv $VENV_DIR
                . $VENV_DIR/bin/activate
                pip install --upgrade pip
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                set -e
                . $VENV_DIR/bin/activate
                python app/app.py
                '''
            }
        }

    }
}