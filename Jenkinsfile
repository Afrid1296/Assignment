pipeline {
    agent any

    environment {
        PYTHON = 'python'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the app...'
                sh "${env.PYTHON} -m py_compile app.py"
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh "pytest tests/"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging...'
                // Simulate deploy
            }
        }

        stage('Manual Approval') {
            steps {
                input message: 'Approve deploy to production?', ok: 'Deploy'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production...'
                // Simulate deploy
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Check logs and notify team.'
        }
    }
}
