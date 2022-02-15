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
                sh '''
                #!/bin/bash
                if ((pm2 restart index.js=="true"))
                then
                echo 'done'
                ''' 
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
