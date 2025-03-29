pipeline {
    agent any
    stages {
        stage('Clonar código') {
            steps {
                git url: 'https://github.com/SSDLC-UR-20251/BankingSystem.git'
            }
        }
        stage('Construir imagen Docker') {
            steps {
                sh 'docker build -t mi_app .'
            }
        }
        stage('Ejecutar contenedor') {
            steps {
                sh 'docker run -d -p 5000:5000 --name mi_app_container mi_app'
            }
        }
        stage('Verificar contenedores') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
