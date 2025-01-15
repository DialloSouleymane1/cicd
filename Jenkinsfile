pipeline{
  agent {
    docker {
      image 'node:21-alpine'
    }
  }
  
  stages{
    stage("Test agent docker"){
      steps{
        sh 'node --version'
        sh 'npm -v'
      }
    }
    stage("Test env variables"){
      steps{
        sh 'printenv'
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