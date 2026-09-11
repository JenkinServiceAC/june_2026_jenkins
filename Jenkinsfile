pipeline {
   agent any

   parameters {
    string (defaultValue: 'main',description: 'provide the branch to build and deploy',name: 'BRANCH',trim: true)
    string (description: 'provide the branch to build and deploy',name: 'BRANCH1',trim: true)
    choice choices: ['dev', 'qa', 'pre-prod', 'prod'], description: 'choose the env to deploy', name: 'Environment'
    booleanParam defaultValue: true, description: 'UNCHECK THIS TO ACTUAL DEPLOY ', name: 'DRY-RUN'

    credentials credentialType: 'com.cloudbees.plugins.credentials.impl.UsernamePasswordCredentialsImpl', defaultValue: 'Class-Github', description: 'github credential', name: 'gitguh', required: true
    password defaultValue: '', description: 'githupassword', name: 'githupassword'
     run description: 'dev server', filter: 'ALL', name: 'Run', projectName: 'dev'
    
    
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