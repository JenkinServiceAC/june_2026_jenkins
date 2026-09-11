pipeline {
    agent {
        label 'slave1'
    }
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
            steps {
                sh 'echo this is Stage2'
            }
        }

        stage('Stage3') {
            steps {
             sh 'echo this is Stage3'  
            }
        }
    }
}