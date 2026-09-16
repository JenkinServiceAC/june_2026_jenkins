pipeline{
    agent any
        stages{
            stage('stage1'){
                steps{
                echo "hello"
                }
            }
        stage('Stage2'){
            steps{
                echo "Stage 2"
                sh'''
                ls -rt
                sleep 5
                '''

            }
        }
        }
}