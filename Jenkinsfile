pipeline{
    agent any
    stages{
        stage('dummy'){
            steps{
                echo env.GIT_BRANCH
                script{
                    echo $(git rev-parse --abbrev-ref HEAD)
                }
            }
        }
        stage('dev')
        {
            when {
                expression {
                    GIT_BRANCH = 'origin/' + sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
                    return GIT_BRANCH == 'origin/develop' || params.FORCE_FULL_BUILD
                }
            }
            steps{
                script {
                        sh "echo 'welcome develop'"
                }
            }
        }
        stage('test'){
            when {
                expression {
                    GIT_BRANCH = 'origin/' + sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
                    return GIT_BRANCH == 'origin/release' || params.FORCE_FULL_BUILD
                }
            }
            steps{
                 script {
                        sh "echo 'welcome release'"
                }
            }
        }
        stage('prod'){
            when {
                expression {
                    GIT_BRANCH = 'origin/' + sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
                    return GIT_BRANCH == 'origin/master' || params.FORCE_FULL_BUILD
                }
            }
            steps{
                script{
                        sh "echo 'welcome prod'"
                }
            }
        }
    }
    
}
