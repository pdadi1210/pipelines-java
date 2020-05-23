pipeline{
    agent any
    stages{
        stage('dummy'){
            steps{
                echo env.GIT_BRANCH
                echo "$env.BRANCH_NAME"
            }
        }
        stage('dev')
        {
            when {
                env.GIT_BRANCH 'origin/development'
            }
            steps{
                script {
                        sh "echo 'welcome develop'"
                }
            }
        }
        stage('test'){
            when {
                env.GIT_BRANCH 'origin/release'
            }
            steps{
                 script {
                        sh "echo 'welcome release'"
                }
            }
        }
        stage('prod'){
            when {
                env.GIT_BRANCH 'originmaster'
            }
            steps{
                script{
                        sh "echo 'welcome prod'"
                }
            }
        }
    }
    
}
