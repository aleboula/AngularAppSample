pipeline {
  agent any
  stages {
    stage('Npm') {
      steps {
        powershell(script: 'npm install', returnStatus: true, returnStdout: true)
      }
    }
    stage('NG build') {
      steps {
        powershell(script: 'ng build', returnStatus: true, returnStdout: true)
      }
    }
  }
  environment {
    Developement = 'DEV'
  }
}