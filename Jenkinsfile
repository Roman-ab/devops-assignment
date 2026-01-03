pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/YOUR_USERNAME/devops-assignment.git'
            }
        }

        stage('Build Docker Images') {
            steps {
                sh '''
                docker build -t backend-app ./backend
                docker build -t frontend-app ./frontend
                '''
            }
        }

        stage('Deploy Using Docker Compose') {
            steps {
                sh '''
                docker-compose down
                docker-compose up -d
                '''
            }
        }
    }

    post {
        success {
            echo "Deployment successful"
        }
        failure {
            echo "Deployment failed"
        }
    }
}
