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
        
     stage('Git') {
        def input_result = input message: 'input branch name for this job', ok: 'ok', parameters: [string(defaultValue: 'master', description: 'branch name', name: 'branch'), string(defaultValue: '', description: 'commit to switch', name: 'commit')]

        sh "echo ${input_result.branch}"
        sh "echo ${input_result.commit}"
    }
        
      }
    }
  }
}
