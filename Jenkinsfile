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
      }
    }
    stage("Test env variables"){
      steps{
        sh 'printenv'
      }
    }
  }
}