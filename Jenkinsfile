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
                sh 'cd /var/lib/jenkins/workspace/krishna sai'
                sh 'npm start'
                echo 'Deployment ssuccessful'

            }
        }
    }
}
