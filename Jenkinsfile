pipeline {
  agent any
  stages {
    stage('Npm') {
      steps {
        powershell(script: 'npm i -g @angular/cli', returnStatus: true, returnStdout: true)
        powershell(script: 'npm install', returnStatus: true, returnStdout: true)
      }
    }
    stage('NG build') {
      steps {
        sh 'ng build'
      }
    }
  }
  environment {
    Developement = 'DEV'
  }
}