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
                
                index=$(pm2 list | grep index | awk '{print $4}')
                status=$(pm2 list | grep index | awk '{print $18}')
                
                check1="index"
                check2="2"

                echo $index
                echo $status

                if [ $index -eq $check1 ] ;then
                    echo "1"

                    if(($status=="online"));then
                        echo "2"
                        pm2 restart index

                        if(($status= "stopped"));then
                            echo "3"
                            pm2 restart index
                        fi
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
            sh 'pm2 restart index.js'
        }
    }    
    
}
