pipeline{
    agent none
    stages{
        stage('dev')
        {
            agent any
            steps{
                script{
                if (env.BRANCH_NAME == "master" && env.CHANGE_ID == null) 
                {
                    sh "echo 'welcome dev conditional'"
                }
                else if (env.BRANCH_NAME == "release" && env.CHANGE_ID == null) 
                {
                    sh "echo 'welcome test conditional'"
                }

                else (env.BRANCH_NAME == "develop" && env.CHANGE_ID == null)
                {
                    sh "echo 'welcome uat conditional'"
                }
                }
                sh "echo 'welcome dev'"
            }
        }
        stage(test){
            agent any
            steps{
                sh "echo 'welcome test'"
            }
        }
        stage("prod"){
            agent any
            steps{
                sh "echo 'welcome uat'"
            }
        }
    }
    
}
