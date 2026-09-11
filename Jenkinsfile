pipeline {
   agent none
    stages {
        stage('Stage1') {
             
            steps {
               sh '''
                #!/bin/bash
                pwd
                sleep 10
                ls -lrt  '''
            }
        }

        stage('Stage2') {
             agent {
        label 'slave1'
    }
            steps {
                sh 'echo this is Stage2'
            }
        }

        stage('Stage3') {
             agent {
        label 'slave2'
    }
            steps {
             sh 'echo this is Stage3'  
            }
        }
        
    }
}