pipeline {
    agent none
    stages {
        stage('Build') {
       agent {
            docker { 
            label 'ec2-fleet' 
            image 'node:16.13.1-alpine' 
            }
        }            
            steps {
                // sh 'whoami'
                sh 'echo $GIT_COMMIT'                
                sh 'sleep 20'
                sh 'node --version'
            }
        }
        stage('Deploy') {
       agent {
            docker { 
            label 'ec2-fleet' 
            image 'node:16.13.1-alpine' 
            }
        }             
            steps {
                sh 'echo $GIT_COMMIT'
                // sh 'whoami'
                sh 'sleep 5'
                sh 'node --version'
            }
        }        
    }
}
