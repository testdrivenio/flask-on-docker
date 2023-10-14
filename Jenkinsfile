pipeline {
    agent any

    environment {
        // Define any environment variables you need
        DOCKERFILE_PATH = './services/web'
        IMAGE_NAME = 'Flask-web'
        TAG_NAME = new Date().format("yyyyMMddHHmmss")
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your version control system
                checkout scm
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
