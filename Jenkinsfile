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
                sh 'echo hello'
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
                sh 'echo hi'
                sh 'printenv'
            }
        }        
    }
}


