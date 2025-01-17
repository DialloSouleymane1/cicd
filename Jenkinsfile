pipeline{
  agent any
  tools {
    nodejs 'nodejs-22-06-0'
  }
  stages{
    stage("Test agent docker"){
      options {
        timestamps()
      }
      steps{
        sh 'npm -v'
      }
    }
  }

  post {
    always {
      echo 'always !' 
    }
    success {
      echo 'success !'
    }
    failure {
      echo 'failure !'
    }
  }
}