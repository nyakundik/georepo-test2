pipeline {
    agent any

    environment{
        BRANCH_NAME = 'main'
        GITHUB_CREDENTIAL = 'github-credential'
        GIT_URL = 'https://github.com/nyakundik/geoapp.git'


    }

    stages{
        stage('os-version'){
            steps{

                sh 'cat /etc/os-release'

            }
        }
        stage('git-checkout'){
            steps{
                git branch: "${BRANCH_NAME}", credentialsId: "${GITHUB_CREDENTIAL}", url: "${GIT_URL}"
            }
        }
       
}
}