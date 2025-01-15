pipeline{
  agent any
  stages{
    stage("Test agent docker"){
      steps{
        sh 'docker -v'
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