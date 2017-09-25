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
    stage('CM') {
      steps {
        parallel(
          "CM": {
            echo 'Tasks for Common and Admin'
            
          },
          "Nuget": {
            build 'EVO-DEV-CM-0. Nuget for CM'
            
          }
        )
      }
    }
  }
}