pipeline {
  agent {
    node {
      label 'docker-slave'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh './distrib.sh build'
        sh 'echo "hello"'
        sh 'hostname'
        sh 'whoami'
        sh 'sleep 15'
      }
    }
  }
}