pipeline{
    agent any
    stages{
        stage('prod')
        {
            when { branch 'master'}
            steps{
                sh "echo 'welcome prod'"
            }
        }
        stage('test'){
            when { branch 'release' }
            steps{
                sh "echo 'welcome test'"
            }
        }
        stage('dev'){
            when { branch 'develop' }
            steps{
                sh "echo 'welcome dev'"
            }
        }
    }
    
}
