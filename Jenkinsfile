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
    stage('setup') {
      steps {
        sh './distrib.sh setup'
      }
    }
  }
}