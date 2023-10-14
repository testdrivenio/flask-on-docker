pipeline {
    agent any

    environment {
        // Define any environment variables you need
        DOCKERFILE_PATH = './services/web'
        IMAGE_NAME = 'Flask-web'
        TAG_NAME = new Date().format("yyyyMMddHHmmss")
    }

    stages {
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
