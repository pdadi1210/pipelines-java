pipeline{
    agent none
    stages{
        stage('prod')
        {
            agent any
            when { env.BRANCH_NAME == 'master'}
            steps{
                sh "echo 'welcome dev'"
            }
        }
        stage('test'){
            agent any
            when { env.BRANCH_NAME == 'release' }
            steps{
                sh "echo 'welcome test'"
            }
        }
        stage('dev'){
            agent any
            when { env.BRANCH_NAME == 'develop' }
            steps{
                sh "echo 'welcome uat'"
            }
        }
    }
    
}
