pipeline{
    agent any
    stages{
        stage('prod')
        {
            when (${env.BRANCH_NAME} == 'master')
            steps{
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
            when (${env.BRANCH_NAME} == 'develop')
            steps{
               script {
                        sh "echo 'welcome develop'"
                }
            }
        }
    }
    
}
