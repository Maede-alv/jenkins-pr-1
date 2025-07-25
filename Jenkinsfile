pipeline {
    agent { docker { image 'docker:24.0.2' args '--privileged -v /var/run/docker.sock:/var/run/docker.sock' } }
    stages {
        stage('Build Image') {
            steps {
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
