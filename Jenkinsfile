pipeline{
  agent {
    docker {
      image 'node:16-alpine'
    }
  }
  stages{
    stage("Test agent docker"){
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