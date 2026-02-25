pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build Backend Docker Image') {
            steps {
                sh 'docker build -t lab6-backend ./backend'
            }
        }

        stage('Run Backend Container') {
            steps {
                sh '''
                    docker rm -f lab6-container || true
                    docker run -d --name lab6-container lab6-backend
                '''
            }
        }

        stage('Verify') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
