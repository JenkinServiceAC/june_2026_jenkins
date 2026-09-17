pipeline{
    agent any
    options{
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '3')
    disableConcurrentBuilds()
    timestamps()
    timeout(time: 4, unit: 'SECONDS')
    ansiColor('xterm')
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
