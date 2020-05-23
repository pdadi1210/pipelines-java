pipeline{
    agent any
    stages{
        stage('prod')
        {
            steps{
                script {
                    if ($BRANCH_NAME == 'master') {
                        sh "echo 'welcome prod'"
                    }
                }
            }
        }
        stage('test'){
            steps{
                script {
                    if ($BRANCH_NAME == 'release') {
                        sh "echo 'welcome test'"
                    }
                }
            }
        }
        stage('dev'){
            when { branch 'develop' }
            steps{
               script {
                    if ($BRANCH_NAME == 'develop') {
                        sh "echo 'welcome develop'"
                    }
                }
            }
        }
    }
    
}
