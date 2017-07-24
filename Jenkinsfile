pipeline {
  agent {
    node {
      label 'jenkins-slave-basic'
    }
    
  }
  stages {
    stage('') {
      steps {
        sh 'Echo "hello"'
        sh '''hostname
'''
        sh 'whoami'
        sh '''sleep 15
'''
      }
    }
  }
}