pipeline {
    agent { label 'ec2-fleet' }
    stages {
        stage('Build') {
       agent {
            docker { 
            image 'node:16.13.1-alpine' 
            reuseNode true
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
            image 'node:16.13.1-alpine' 
            reuseNode true                
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

