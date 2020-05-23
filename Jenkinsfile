pipeline{
    agent any
    stages{
        stage('dev')
        {
            when {
				      expression {env.GIT_BRANCH == 'origin/develop'}
            }
            steps{
                script {
                        sh "echo 'welcome develop'"
                }
            }
        }
        stage('test'){
            when {
				      expression {env.GIT_BRANCH == 'origin/release'}
            }
            steps{
                 script {
                        sh "echo 'welcome release'"
                }
            }
        }
        stage('prod'){
            when {
				      expression {env.GIT_BRANCH == 'origin/master'}
            }
            steps{
                script{
                        sh "echo 'welcome prod'"
                }
            }
        }
    }
    
}
