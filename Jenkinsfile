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
                sh 'ssh -i "/var/lib/jenkins/dockertest.pem" ubuntu@ec2-3-111-150-61.ap-south-1.compute.amazonaws.com'
                sh 'cd /var/lib/jenkins/workspace/nodejs'
                sh 'pm2 start index.js'
                echo 'Deployment ssuccessful'
                
            }
        }
    }
}
