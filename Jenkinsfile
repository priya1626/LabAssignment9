pipeline {
    agent any

    environment {
        IMAGE_NAME = "docker-images"
        CONTAINER_NAME = "docker-container"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                bat "docker build -t priyamvada1626/%IMAGE_NAME% ."
            }
        }

        stage('Verify Docker Image') {  
            steps {
                bat "docker images"
            }
        }
        
        stage('Login to Docker Hub') {
            steps {
                bat 'docker login -u "priyamvada1626" -p "Varsha1626@" docker.io'
            }
        }
        
        stage('Push to Docker Hub') {
            steps {
                bat 'docker push priyamvada1626/%IMAGE_NAME%'
            }
        }

        // stage('Run Docker Container') {
        //     steps {
        //         bat 'docker run -d --name %CONTAINER_NAME% priyamvada1626/%IMAGE_NAME%'
        //     }
        // }
    }
}
