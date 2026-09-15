pipeline {
    agent any

    stages {
        stage('STAGE1') {
            steps {
               sh '''
                exit 1
                '''
            }
        }

        stage('STAGE2') {
            steps {
                sleep 5
            }
        }

        stage('STAGE3') {
            steps {
                sleep 5
            }
        }
    }
}