pipeline {
  agent any
  stages {
    stage('autotest') {
      parallel {
        stage('autotest') {
          environment {
            gitname = 'yes'
          }
          steps {
            sh ' echo "hello test!"'
          }
        }
        stage('print') {
          steps {
            sh 'echo $gitname'
          }
        }
      }
    }
  }
}