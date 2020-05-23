pipeline{
    agent any
    stages{
        stage('prod')
        {
            steps{
                script {
                    if("$env.BRANCH_NAME" == 'master'){
                        sh "echo 'welcome prod'"
                    }
                }
            }
        }
        stage('test'){
            steps{
                script {
                        if("$env.BRANCH_NAME" == 'release'){
                        sh "echo 'welcome prod'"
                    }
                }
            }
        }
        stage('dev'){
            steps{
               script {
                       if("$env.BRANCH_NAME" == 'develop'){
                        sh "echo 'welcome prod'"
                    }
                }
            }
        }
    }
    
}
