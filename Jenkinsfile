pipeline{
    agent {
        label 'slave5'
    }
    stages{
        stage('build'){
            steps{
                echo "Slave2 build"
            }
        }

        stage('Test'){
            steps{
             echo "This is test buil"
            }
        }
        stage('Deploy'){
            steps{
                echo "This is Deploy"
            }
        }

    }
}