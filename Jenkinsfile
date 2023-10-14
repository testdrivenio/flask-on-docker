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
                    withCredentials([string(credentialsId: 'github', variable: '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')]) {
                    docker.build("${env.IMAGE_NAME}:${env.TAG_NAME}", "-f ${env.DOCKERFILE_PATH} .")
                }
            }
        }
  }
}