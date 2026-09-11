pipeline {
   agent any

   parameters {
    string defaultValue: 'main',
    description: 'provide the branch to build and deploy',
    name: 'BRANCH',
    trim: true
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