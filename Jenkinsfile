pipeline {
    agent any
    stages {
        stage('Build Image') {
            steps {
                sh 'docker --version'
                sh 'docker build -t my-microservice:latest ./microservice-app'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 my-microservice:latest'
            }
        }
    }
}
