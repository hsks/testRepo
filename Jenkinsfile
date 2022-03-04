pipeline {
    agent none
//     options {
//             skipDefaultCheckout()
//         }    
    stages {
        stage('Build') {
       agent {
            docker { 
            label 'ec2-fleet'  
            image 'node:16.13.1-alpine'
            reuseNode true
            }
        }            
            steps {
                // sh 'whoami'
                sh 'echo $GIT_COMMIT'                
                sh 'printenv'
                sh 'sleep 20'
                sh 'node --version'
            }
        }
        stage('Deploy') {
       agent {
            docker { 
            label 'ec2-fleet'    
            image 'node:16.13.1-alpine' 
            reuseNode true                
            }
        }             
            steps {     
                sh 'echo $GIT_COMMIT'
                // sh 'whoami'
                sh 'sleep 5'
                sh 'node --version'
                sh 'printenv'
            }
        }        
    }
}
