pipeline {
  agent any
  stages {
    stage('Npm') {
      steps {
        powershell(script: 'npm install -g @angular/cli', returnStatus: true, returnStdout: true)
        powershell(script: 'npm install', returnStatus: true, returnStdout: true)
      }
    }
    stage('NG install verification') {
      steps {
        sh 'node_modules/.bin/ng -v'
      }
    }
    stage('NG build') {
      steps {
        sh 'node_modules/.bin/ng build'
      }
    }
  }
  environment {
    Developement = 'DEV'
  }
}