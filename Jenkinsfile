pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/jhoan2000/proyecto-jenkins.git'
            }
        }

        stage('Ejecutar Pruebas') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install -r requirements.txt
                    python -m unittest
                '''

            }
        }

        stage('Desplegar (Opcional)') {
            steps {
                echo 'Aquí puedes agregar comandos para desplegar tu aplicación'
            }
        }
    }
}
