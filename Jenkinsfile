pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git  branch: 'main', url: 'https://github.com/jhoan2000/proyecto-jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                python3 -m venv venv
                source venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                sh '''
                source venv/bin/activate
                pytest tests/
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Agrega aquí los pasos para desplegar la app
            }
        }
    }
}
