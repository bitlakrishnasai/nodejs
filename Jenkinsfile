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
                
                index = pm2 list | grep index | awk '{print $4}'
                status = pm2 list | grep index | awk '{print $18}'
                
                if (($index=="index"))
                then
                    if (($status = "online"))
                    then
                        pm2 restart index
                    else
                        pm2 restart index
                    fi
                else
                    pm2 start index.js
                fi
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
