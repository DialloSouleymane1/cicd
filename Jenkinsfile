pipeline{
  agent any
  stages{
    stage("Test env variables"){
      steps{
        echo "BRANCH_NAME: ${env.BRANCH_NAME}"
        echo "CI: ${env.CI}"
        echo "BRANCHE_IS_PRIMARY: ${env.BRANCHE_IS_PRIMARY}"
        echo "BUILD_NUMBER: ${env.BUILD_NUMBER}"
        echo "JENKINS_URL: ${env.JENKINS_URL}"
      }
    }
  }
}