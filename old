pipeline{
  agent any
  parameters {
    string(name: 'NAME', defaultValue: 'Souley Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
  }
  stages{
    stage("Build"){
      options{
        timestamps()
      }
      steps{
        echo "Hello ${params.NAME}"
        echo "Biography: ${params.BIOGRAPHY}"
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