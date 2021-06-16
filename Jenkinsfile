pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sleep 10
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        build job: 'paramjob', parameters: [string(name: 'year', value: '2010'), string(name: 'month', value: 'Sep')]
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        build 'thirdjob'
        // build job: 'thirdjob'
      }
    }
  }
}
