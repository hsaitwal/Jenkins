pipeline {
  agent any
  stages {
    stage('Initiate') {
      steps {
        echo 'Job Initiated '
        sleep 10
      }
    }
    stage('Master') {
      steps {
        build(job: 'Test1', quietPeriod: 7, wait: true, propagate: true)
      }
    }
  }
}