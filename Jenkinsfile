pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                bat 'echo Building the app...'
                // Replace with your actual build commands for Windows
            }
        }
        stage('Test') {
            steps {
                bat 'echo Running tests...'
                // Replace with your actual test commands for Windows
            }
        }
        stage('Deploy to Staging') {
            steps {
                bat 'echo Deploying to Staging...'
                // Replace with your actual deployment commands for Windows
            }
        }
        stage('Manual Approval') {
            steps {
                input 'Approve deployment to Production?'
            }
        }
        stage('Deploy to Production') {
            steps {
                bat 'echo Deploying to Production...'
                // Replace with your actual deployment commands for Windows
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished!'
        }
    }
}
