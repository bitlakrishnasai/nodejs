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
        stage('Deployment') {
            steps {
                sh 'pm2 start index.js'
                echo 'Deployment successful'
                
            }
        }
    }
}
