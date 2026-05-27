pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/muskan922/react-jenkins.git'
            }
        }

        stage('Build Docker Containers') {
            steps {
                bat 'docker compose build'
            }
        }

        stage('Stop Old Containers') {
            steps {
                bat 'docker compose down'
            }
        }

        stage('Start New Containers') {
            steps {
                bat 'docker compose up -d'
            }
        }
    }
}