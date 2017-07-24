pipeline {
  agent {
    node {
      label 'jenkins-slave-basic'
    }
    
  }
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
  }
}