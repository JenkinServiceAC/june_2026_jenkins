pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               sh '''
                #!/bin/bash
                pwd
                sleep 10
                ls -lrt '''
            }
        }

        stage('Test') {
            steps {
                sh 'echo this is Test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application.'
            }
        }
    }
}