pipeline {
  agent any
  stages {
    stage('use matrix') {
      matrix {
        axes {
          axis{
            name 'PLATFORM'
            values 'linux', 'windows'
          }
          axis {
            name 'BROWSER'
            values 'chrome', 'firefox'
          }
        }
        stages {
          stage('build') {
            steps {
              echo "Building ${PLATFORM} on ${BROWSER}"
            }
          }
          stage('Test') {
            steps {
              echo "Testing ${PLATFORM} on ${BROWSER}"
            }
          }
        }
      }
    }
  }
}