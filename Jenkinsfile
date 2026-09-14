pipeline{
    agent any
parameters {
  string (defaultValue: 'main', description: 'Provide the branch to build and deploy', name: 'BRANCH', trim: true)
  choice(choices: ['dev', 'test', 'pre-pod', 'PROD'], 
  description: 'List all the environments',
   name: 'ENVIRONMENT')
}

    stages{
        stage('build'){
            steps{
                echo " build"
                sh '''echo BRANCH - $BRANCH
                sleep 5'''
                echo "${params.ENVIRONMENT}"
            }
        }

        stage('Test'){
            steps{
             echo "This is test buil"
             echo "${params.BRANCH}"
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