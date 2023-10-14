pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Jenkins Pipeline'
      }
    }
    stage('Build Docker Image') {
            steps {
                script {
                    // Build the Docker image using the Dockerfile
                    docker.build("${env.IMAGE_NAME}:${env.TAG_NAME}", "-f ${env.DOCKERFILE_PATH} .")
                }
            }
        }
  }
}