pipeline{
    agent none
    stages{
        stage('prod')
        {
            agent any
            when { branch 'master'}
            steps{
                sh "echo 'welcome prod'"
            }
        }
        stage('test'){
            agent any
            when { branch 'release' }
            steps{
                sh "echo 'welcome test'"
            }
        }
        stage('dev'){
            agent any
            when { branch 'develop' }
            steps{
                sh "echo 'welcome dev'"
            }
        }
    }
    
}
