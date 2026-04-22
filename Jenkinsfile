pipeline {
    agent any

    stages {

        stage('Setup Virtual Env') {
            steps {
                sh 'python3 -m venv venv'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'venv/bin/pytest'
            }
        }

        stage('Run App') {
            steps {
                sh 'venv/bin/python app.py'
            }
        }
    }
}