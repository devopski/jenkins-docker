pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Docker image..'
                sh "docker build -t devopski/jenkins-docker ."
                
                // REPLACE with your DockerHub repo name
                // sh "docker build -t [your repo name] ."
            }
        }
        stage('Push') {
            steps {
                echo 'Pushing Docker image to registry..'
                sh "docker push devopski/jenkins-docker"
                
                // REPLACE with your DockerHub repo name
                // sh "docker push [your repo name]"
            }
        }
    }
}
