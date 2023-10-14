pipeline {
  agent any
  stages {
    stage('Checkout') {
            steps {
                checkout scm
            }
        }

    stage('Build') {
      steps {
        echo 'Starting to build docker image'
        script {
          sh 'docker build -t flaskapp:latest .'
        }
      }
    }

  }
} 