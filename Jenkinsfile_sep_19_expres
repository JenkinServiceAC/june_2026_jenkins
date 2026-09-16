pipeline{
    agent any
    stages{

        stage('STAGE1'){
            when {
                expression{
                env.GIT_BRANCH=='origin/main'
                }
            }
            steps{
                echo "${env.BUILD_NUMBER}"  
                echo "${env.GIT_BRANCH}"
                echo "${env.JOB_NAME}"
                echo "${env.GIT_URL}"
                echo "${env.BRANCH_NAME}"           
           }
        }
    }
}