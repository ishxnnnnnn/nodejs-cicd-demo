pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ishxnnnnnn/nodejs-cicd-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t jenkins-demo-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
                sh '''
                docker stop jenkins-demo || true
                docker rm jenkins-demo || true
                docker run -d -p 3000:3000 --name jenkins-demo jenkins-demo-app
                '''
            }
        }
    }

    post {
        success {
            echo '✅ CI/CD Pipeline executed successfully'
        }
        failure {
            echo '❌ Pipeline failed'
        }
    }
}
