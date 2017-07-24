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
            sh 'echo "hello"'
            sh 'hostname'
            sh 'whoami'
            sh 'sleep 15'
            
          },
          "test_connection": {
            sh './distrib.sh test_connection'
            
          }
        )
      }
    }
  }
}