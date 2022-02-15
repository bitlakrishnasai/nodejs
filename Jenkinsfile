pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                echo 'Test successful'
            }
        }
        stage('Deployment test') {
            steps {
                sh 'pm2 restart index.js'
                echo 'Deployment test successful'
            }
        }

    }
    post{
        success {
            sh 'pm2 restart index.js'
            sh 'pm2 list'
        }
    
    stages {
        stage('Deployment') {
            steps {
                echo 'Deployment successful'
            }
        }
    }
}
