pipeline {
    agent any
 parameters {
    string (defaultValue: 'main',description: 'provide the branch to build and deploy',name: 'BRANCH',trim: true)
    choice choices: ['dev', 'qa', 'pre-prod', 'prod'], description: 'choose the env to deploy', name: 'ENVIRONMENT'
      booleanParam defaultValue: true, description: 'DRY_RUN', name: 'DRY_RUN'
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
                sh '''
                    echo APP - $APP 
                    echo BRANCH - $BRANCH
                    sleep 10
                    ls -lrt
                '''

                echo "${env.BRANCH}"
            }
        }

        stage('STAGE3') {
            steps {
                sh '''
                echo "This is Stage3"
                
                echo "BRANCH : ${BRANCH}"
                echo "DRY_RUN: ${DRY_RUN}"
                echo "ENVIRONMNET : $ENVIRONMENT "

                '''
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