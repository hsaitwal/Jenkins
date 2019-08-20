pipeline {
  agent any
  stages {
    stage('Initiate') {
      steps {
        echo 'Job Initiated '
        sleep 10
      }
    }
    stage('Check Node status') {
      steps {
        node(label: 'master') {
          build(job: 'FRB_Revert_Server_Snapshot', quietPeriod: 90, wait: true)
          echo 'Reverting is in Progress'
        }

      }
    }
    stage('End') {
      steps {
        echo 'End'
      }
    }
  }
}