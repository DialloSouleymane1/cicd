pipeline{
  agent any
  stages{
    stage("Build"){
      options{
        timestamps()
      }
      steps{
        echo "Build succefully !"
      }
    }

    stage("Deploy"){

      options{
        timestamps()
      }
      input {
        message "Should we continue?"
        ok "Yes, we should."
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should deploy this?')
          string(name: 'VERSION', defaultValue: 'latest', description: 'Latest version to be deployed')
        }
        submitter 'souley'
        submitterParameter 'USER_SUBMIT'
      }
      steps{
        echo "should deploy user: ${PERSON}"
        echo "Version to be deployed: ${VERSION}"
        echo "User who deployed : ${USER_SUBMIT}"
        echo "Deployed succefully !"
      }
    }
  }
}