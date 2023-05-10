pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Compilando..."'
                sh 'docker build -t MmartinezV2/go-web-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Probando..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Desplegando..."'
            }
        }
    }
}
