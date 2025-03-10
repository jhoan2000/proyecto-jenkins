pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                git  branch: 'main', url: 'https://github.com/jhoan2000/proyecto-jenkins.git'
            }
        }

       
        stage('Ejecutar Pruebas') {
            steps {
                sh 'source venv/bin/activate && pytest tests/'  // Ejecutar pruebas unitarias
            }
        }

        stage('Desplegar (Opcional)') {
            steps {
                echo 'Aquí puedes agregar comandos para desplegar tu aplicación'
            }
        }
    }
}
