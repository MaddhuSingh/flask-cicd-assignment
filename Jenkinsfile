pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/MaddhuSingh/flask-cicd-assignment.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }

        stage('Run App') {
            steps {
                bat 'python app.py'
            }
        }
    }
}