pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                git https://github.com/jhoan2000/proyecto-jenkins.git
            }
        }

        stage('Configurar Entorno') {
            steps {
                sh 'python3 -m venv venv'  // Crear entorno virtual
                sh 'source venv/bin/activate && pip install -r requirements.txt'  // Instalar dependencias
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
