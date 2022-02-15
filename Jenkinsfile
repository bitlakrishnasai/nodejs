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
                sh 'pm2 start index.js | pm2 restart index.js'
                echo 'Deployment test successful'
            }
        }

    }
    post{
        success {
            sh 'pwd'
            sh 'pm2 restart index.js'
            sh 'pm2 list'
        }
    }    
    
}
