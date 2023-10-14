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
          def dockerImage = docker.build("flask/web:latest")
          dockerImage.withDockerfile('flask-on-docker/services/web')
        }
      }
    }
  }
} 