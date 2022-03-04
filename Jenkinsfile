pipeline {
    agent none
//     options {
//             skipDefaultCheckout()
//         }    
    stages {
        stage('Build') {
       agent {
            label 'ec2-fleet'  
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
            label 'ec2-fleet'                
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

