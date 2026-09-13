pipeline {
    agent any
 parameters {
    string (defaultValue: 'main',description: 'provide the branch to build and deploy',name: 'BRANCH',trim: true)
    choice choices: ['dev', 'qa', 'pre-prod', 'prod'], description: 'choose the env to deploy', name: 'ENVIRONMENT'
      
  run filter: 'COMPLETED', name: 'run ', projectName: 'run1'

        }
    environment {
        BRANCH = 'main'
    }
    stages {
        stage('STAGE1 harsha sir') {
            environment {
                APP = 'frontend'
            }
            steps {
                sh '''
                    echo APP - $APP 
                    echo BRANCH - $BRANCH
                    sleep 5
                '''
            }
        }

        stage('STAGE2') {
          
            steps {
                echo "${env.BRANCH}"
            }
        }

        stage('STAGE3') {
            steps {
                
                echo "This is Stage3"
                
                echo "BRANCH : ${params.BRANCH}"
                echo "DRY_RUN: ${params.DRY_RUN}"
                echo "ENVIRONMNET : ${params.ENVIRONMENT}"
                echo "run : ${params.run}"

                
            }
        }

        stage('STAGE4') {
            steps {
                 sh 'echo THis is STAGE4'
                 sh 'sleep 5'
            }
        }
    }
}