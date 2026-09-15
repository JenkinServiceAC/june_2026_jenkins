def stage1status=''

pipeline{
    agent any
    stages{
        stage('STAGE1'){
          steps  {

                script{
                    try {

                        sh '''
                        echo 'stage1 success'
                        sleep 5
                        
                        '''
                        currentBuild.result='SUCCESS'
                    }catch(Exception e){
                        echo "Coaught exception: ${e.message}"
                        currentBuild.result = 'FAILURE'
                    }
                }    

            }   
        }
            stage('STAGE2'){
                when {
                    expression{
                        currentBuild.result == 'SUCCESS'

                    }
                }
                steps{
                    echo 'Stage 1 is success'
                }

            }
            stage('STAGE3'){
                when{
                    expression{
                        currentBuild.result == 'FAILURE'

                    }
                }
                steps{

                    echo 'STAGE1 is FAILED'
                }
            }

        }

    }





