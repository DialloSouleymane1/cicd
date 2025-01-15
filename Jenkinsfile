pipeline{
  agent {
    docker {
      image 'node:latest'
    }
  }
  stages{
    stage("Test agent docker"){
      steps{
        sh 'node --version'
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