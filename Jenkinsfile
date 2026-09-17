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
            
        stage('Parallel Test Stage2'){
            parallel {
                stage('Unit Test'){
                    steps{
                        echo "Stage 2"
                        sh'''
                        ls -rt
                        sleep 5
                        '''
                        echo "Running Unit testing"
                    }
                }
                stage('Integration Test'){
                    steps{
                        echo "Running Integration test"
                    }
                }
                stage('security scane'){

                    steps{

                        sh 'pwd'
                        sleep 5
                        echo ' Running security scan'
                    }
                }

            }
            stage('Deploy'){

                steps{
                    echo 'Deploying application'
                }
            }
        }
    }
}