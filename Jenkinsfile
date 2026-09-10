pipeline {
    agent any

    stages {
        stage('Stage1') {
            steps {
               bat '''
                #!/bin/bash
                pwd
                sleep 10
                ls -lrt '''
            }
        }

        stage('Stage 2') {
            steps {
                bat 'echo this is Test'
            }
        }

        stage('Stage 3') {
            steps {
               
            }
        }
    }
}