pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building from Jenkinsfile...'
        sleep 10
      }
    }
    stage('Test') {
      steps {
        echo 'Testing from Jenkinsfile...'
        build job: 'paramjob', parameters: [string(name: 'year', value: '2010'), string(name: 'month', value: 'Sep')]
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying from Jenkinsfile...'
        build 'thirdjob'
        // build job: 'thirdjob'
      }
    }
  }
}
