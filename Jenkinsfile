pipeline{
    agent any
    stages{
        stage('dummy'){
            steps{
                echo env.GIT_BRANCH
                echo branch
            }
        }
        stage('dev')
        {
            when {
                branch 'origin/development'
            }
            steps{
                script {
                        sh "echo 'welcome develop'"
                }
            }
        }
        stage('test'){
            when {
                branch 'origin/release'
            }
            steps{
                 script {
                        sh "echo 'welcome release'"
                }
            }
        }
        stage('prod'){
            when {
                branch 'originmaster'
            }
            steps{
                script{
                        sh "echo 'welcome prod'"
                }
            }
        }
    }
    
}
