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
                sh 'export BUILD_ID=dontKillMePlease'
                sh 'pm2 start index.js'
                echo 'Deployment ssuccessful'
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
