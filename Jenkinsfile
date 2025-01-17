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
        submiter 'admin'
        submitParameter 'USER_SUBMIT'
      }
      steps{
        echo "should deploy user: ${params.PERSON}"
        echo "Version to be deployed: ${params.VERSION}"
        echo "User who deployed : ${USER_SUBMIT}"
        echo "Deployed succefully !"
      }
    }
  }
}