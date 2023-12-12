pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Clone the Git repository
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/Awan/multi-tier-app.git']]])
                }
            }
        }

        stage('Build and Push to Docker Hub') {
            steps {
                script {
                    // Build and push the backend Docker image
                    // docker.build("abdullahkhabir/backend", "-f backend/Dockerfile .")
                    // docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_credentials') {
                    //    docker.image("abdullahkhabir/backend").push()
                    sh 'docker-compose up'

                    // Build and push the frontend Docker image
                    // docker.build("abdullahkhabir/frontend", "-f frontend/public/Dockerfile .")
                    // docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_credentials') {
                    //    docker.image("abdullahkhabir/frontend").push()
                    echo "leaving it blank for now"
                }
            }
        }

        stage('Deploy with Docker Compose') {
            steps {
                script {
                    sh 'echo hello done'
                }
            }
        }
    }

    post {
        success {
            echo 'Build, Push, and Deploy successful'
        }
        failure {
            echo 'Build, Push, or Deploy failed'
        }
    }
}

