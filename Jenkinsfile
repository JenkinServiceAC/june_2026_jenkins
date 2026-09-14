pipeline{
    agent any
    environment {

        BRANCH = 'main'
    }
    stages{
        stage('build'){
            steps{
                echo " build"
                sh '''echo BRANCH - $BRANCH
                sleep 5'''
            }
        }

        stage('Test'){
            steps{
             echo "This is test buil"
             echo ${env.BRANCH}
             sleep 5
            }
        }
        stage('Deploy'){
            steps{
                echo "This is Deploy"
            }
        }

    }
}