pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Pipeline start'
      }
    }
    stage('IIS') {
      steps {
        build 'EVO-DEV-IIS-Wix.msi'
      }
    }
  }
}