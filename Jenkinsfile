pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/chigullanaveen-cell/my-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh '''
                docker stop devops-container || true
                docker rm devops-container || true
                docker run -d -p 8081:80 --name devops-container devops-app
                '''
            }
        }
    }
}
