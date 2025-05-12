pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "school-app:latest"
    }
    stages {
        stage('Clonage') {
            steps {
                git branch: 'main', 
                url: 'https://github.com/IramKsila24/test.git'
            }
        }
        stage('Building mvn') {
            steps {
                sh 'mvn clean install'
            }
        }
stage('Docker Image ') {
 steps {
 sh 'docker build -t school-app:latest .'
 }
 }
 }
}
