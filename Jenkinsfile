pipeline {
  agent none
  stages {
    stage('IIS') {
      steps {
        parallel(
          "IIS": {
            build 'EVO-DEV-IIS-Wix.msi'
            
          },
          "CM": {
            build 'EVO-DEV-CM-0. Nuget for CM'
            build 'EVO-DEV-CM-1. Src'
            build 'EVO-DEV-CM-2.Wix'
            
          }
        )
      }
    }
  }
}