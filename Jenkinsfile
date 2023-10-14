pipeline {
  agent any
  stages {
    stage('Checkout') {
            steps {
                checkout scm
            }
        }

    stage('Build Docker Image') {
      steps {
        echo 'Starting to build docker image'
        script {
          sh 'docker build -t flaskapp:latest .'
        }
      }
      
    }
  }
} 