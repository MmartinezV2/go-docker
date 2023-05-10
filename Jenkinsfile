pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                sh 'docker build -t mmartinezv2/go-web-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing local deploy ..."'
		sh 'cd /home/jenkins; git clone https://github.com/MmartinezV2/go-docker.git'
		sh 'cd /home/jenkins/go-docker; docker compose up -d'
                sh 'echo "Do some tests..."'
                sh 'echo "Remove environment test..."'
		sh 'cd /home/jenkins/go-docker; docker compose down'
		sh 'rm -rf /home/jenkins/go-docker'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy..."'
            }
        }
    }
}
