pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Docker image..'
                docker build -t devopski/jenkins-docker .
                
            }
        }
        stage('Push') {
            steps {
                echo 'Pushing Docker image to registry..'
                docker push devopski/jenkins-docker
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                docker run -d -p 80:80 devopski/jenkins-docker
            }
        }
    }
}