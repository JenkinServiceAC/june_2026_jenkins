pipeline{
    agent {
        label 'slave2'
    }
    stages{
        stage('build'){
            step{
                echo "Slave1 build"
            }
        }

        stage('Test'){
            step{
             echo "This is test buil"
            }
        }
        stage('Deploy'){
            step{
                echo "This is Deploy"
            }
        }

    }
}