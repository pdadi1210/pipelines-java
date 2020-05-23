pipeline{
    agent any
    stages{
        stage('prod')
        {
            steps{
                script {
                    if(env.GIT_BRANCH == 'develop'){
                        sh "echo 'welcome develop'"
                    }
                }
            }
        }
        stage('test'){
            steps{
                 script {
                     if((env.GIT_BRANCH == 'release'){
                        sh "echo 'welcome release'"
                     }
                }
            }
        }
        stage('dev'){
            steps{
                script{
                    if(env.GIT_BRANCH == 'master') {
                        sh "echo 'welcome prod'"
                    }
                }
            }
        }
    }
    
}
