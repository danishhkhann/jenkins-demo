pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo:latest .'
            }
        }

        stage('Check Docker Image') {
            steps {
                sh 'docker images jenkins-demo'
            }
        }
    }

    post {
        success {
            echo 'Docker image built successfully!'
        }

        failure {
            echo 'Docker build failed!'
        }

        always {
            echo 'Pipeline finished'
        }
    }
}
