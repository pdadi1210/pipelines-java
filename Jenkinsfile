pipeline{
    agent none
    stages{
        stage('dev')
        {
            agent any
            steps{
                if ($BRANCH_NAME == "master" && $CHANGE_ID == null) 
                {
                    sh "echo 'welcome dev conditional'"
                }
                else if ($BRANCH_NAME == "release" && $CHANGE_ID == null) 
                {
                    sh "echo 'welcome test conditional'"
                }

                else ($BRANCH_NAME == "develop" && $CHANGE_ID == null)
                {
                    sh "echo 'welcome uat conditional'"
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
