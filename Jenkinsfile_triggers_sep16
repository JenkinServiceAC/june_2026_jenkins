pipeline{
    agent any
    triggers{
        // cron('H/5 * * * *')
        pollSCM('H */4 * * 1-5')
    }
        stages{
            stage('stage1'){
                steps{
            sh 'pwd'
            sh '''ls -rt
            sleep 5 '''
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