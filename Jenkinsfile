pipeline {
  agent any

  stages {
    stage("One") {
      steps {
        echo "Hello"
      }
    }
    stage("Evaluate Master") {
      when {
         expression {env.GIT_BRANCH == 'origin/master'}
      }
      steps {
        echo "World"
        echo "Heal it"
      }
    }
  }
}
