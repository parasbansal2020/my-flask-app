pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/my-flask-app.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh './venv/bin/pip install --upgrade pip'
                sh './venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh './venv/bin/python -m pytest test_app.py'
            }
        }

        stage('Run Flask') {
            steps {
                echo 'Application would be deployed here'
                // You can later add Docker or server deploy
            }
        }
    }
}
