pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/varadharajs/devops-project-01.git'
            }
        }

        stage('Check Files') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-project-01 .'
            }
        }

        stage('Deploy Application') {
            steps {
                sh '''
                    docker stop devops-app || true
                    docker rm devops-app || true
                    
                    docker run -d \
                    -p 8081:80 \
                    --name devops-app \
                    devops-project-01
                '''
            }
        }

    }
}
