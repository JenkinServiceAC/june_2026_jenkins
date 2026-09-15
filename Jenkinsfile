pipeline {
    agent any

    stages {
        stage('STAGE1') {
            steps {
                catchError(buildResult:'SUCCESS',stageResult:'FAILURE'){
                sh '''
                echo "Running Tests"
                exit 1
                '''

                }
             
            }
        }

        stage('STAGE2') {
            steps {
                sleep 5
                echo "TEST stage is running"
            }
        }

        stage('STAGE3') {
            steps {
                sleep 5
                echo "Deploy stage is running"
            }
        }
    }
}