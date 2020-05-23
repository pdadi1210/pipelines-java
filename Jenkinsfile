pipeline{
    agent any
    stages{
        stage{
            steps{
                echo env.GIT_BRANCH
            }
        }
        stage('prod')
        {
            when {
                branch 'development'
            }
            steps{
                script {
                        sh "echo 'welcome develop'"
                }
            }
        }
        stage('test'){
            when {
                branch 'release'
            }
            steps{
                 script {
                        sh "echo 'welcome release'"
                }
            }
        }
        stage('dev'){
            when {
                branch 'master'
            }
            steps{
                script{
                        sh "echo 'welcome prod'"
                }
            }
        }
    }
    
}
