pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("myapp:latest")
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    dockerImage.run('-d -p 8080:8080')
                }
            }
        }
        stage('clone'){
            steps {
                script {
                    git clone ""C:\Users\priya\OneDrive\Desktop\jenkins\LabAssignment9  "
                }
            }
        }
    }
}
