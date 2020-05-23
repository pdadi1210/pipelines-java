pipeline{
    agent any
    stages{
        stage('prod')
        {
            steps{
                when (${env.BRANCH_NAME} == 'master')
                script {
                        sh "echo 'welcome prod'"
                }
            }
        }
        stage('test'){
            steps{
                when (${env.BRANCH_NAME} == 'release')
                script {
                        sh "echo 'welcome test'"
                }
            }
        }
        stage('dev'){
            when (${env.BRANCH_NAME} == 'master')
            steps{
               script {
                        sh "echo 'welcome develop'"
                }
            }
        }
    }
    
}
