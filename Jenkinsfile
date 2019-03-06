pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        git(url: 'git credentialsId: \'github\', url: \'https://github.com/aleboula/AngularAppSample.git\'', branch: 'master', changelog: true, poll: true)
      }
    }
    stage('Npm') {
      steps {
        powershell(script: 'npm install', returnStatus: true, returnStdout: true)
      }
    }
  }
  environment {
    Developement = 'DEV'
  }
}