pipeline{
    agent any
    stages{
        stage('Clone repo'){
            steps{
                git branch: 'main', url: 'https://github.com/lax2k3/DevOps-Project-Two-Tier-Flask-App.git'
            }
        }
        stage('Build image'){
            steps{
                sh 'docker build -t flask-app .'
            }
        }
        stage('Deploy with Docker Compose') {
    steps {
        sh 'docker compose down || true'
        sh 'docker compose up -d'
            }
        }
    }
}
