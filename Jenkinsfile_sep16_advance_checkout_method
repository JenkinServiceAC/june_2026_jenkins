pipeline{
    agent any
        stages{
            stage('stage1'){
                steps{
            sh 'pwd'
            checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                    credentialsId: 'Class-Github',
                    url: 'https://github.com/Nirmala18/calculator_fork.git'
    ]]
])
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