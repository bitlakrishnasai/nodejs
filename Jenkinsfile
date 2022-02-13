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
                ls -a
                npm start
                echo 'Deployment successful'
            }
        }
    }
}
