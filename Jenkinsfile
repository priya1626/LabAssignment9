pipeline {
    agent any

    environment {
        IMAGE_NAME = "docker-images"
        CONTAINER_NAME = "docker-container"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                bat "docker build -t %IMAGE_NAME% ."
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d --name %CONTAINER_NAME% %IMAGE_NAME%'
            }
        }
    }
}
