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
                echo 'Build successful'
            }
        }
        stage('Deployment') {
            steps {
                
                sh 'pm2 start index.js'
                echo 'Deployment ssuccessful'
                export BUILD_ID=dontKillMePlease
            }
        }
        
        stage('Deployment test') {
            steps {
                sh 'pm2 list'
                echo 'Deployment test ssuccessful'
            }
        }
    }
}
