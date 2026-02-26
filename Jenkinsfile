pipeline {
    agent any

    stages {

        stage('Build Backend Image') {
            steps {
                sh 'docker build -t backend-app backend'
            }
        }

        stage('Deploy Backends') {
            steps {		
                sh '''
                docker rm -f backend1 backend2 nginx-lb || true
                docker network rm lab6-network || true
                docker network create lab6-network

              
