pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh './distrib.sh build'
            
          },
          "test_connection": {
            sh './distrib.sh test_connection'
            
          }
        )
      }
    }
    stage('copy') {
      steps {
        sh './distrib.sh copy'
      }
    }
  }
}