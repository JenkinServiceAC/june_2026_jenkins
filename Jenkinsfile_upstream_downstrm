pipeline{
    agent any
    triggers { upstream(upstreamProjects: 'freestyle,freestyle_test1', threshold: hudson.model.Result.SUCCESS) 
   }
        stages{
            stage('stage1'){
                steps{
                    ansiColor('xterm') {
            sh 'pwd'
            sh '''ls -rt
            sleep 5 '''
                }
                }
            }
            
        stage('Stage2'){
        steps{

            sh '''
            pwd
            ls -lrt
            '''
        }
        }
            stage('Deploy'){

                steps{
                    echo 'Deploying application'
                }
            }
        }
}
