// Using git without checkout 
pipeline {
  agent any
  environment {
    GIT_SSH_COMMAND='ssh -vvv'
    GIT_CURL_VERBOSE=1
    GIT_TRACE=1
  }
  stages {
    stage('Checkout') {
      steps {
        sh 'printenv'
        git branch: 'master', url: 'git@github.com:cbdchang/simple-java-maven-app.git', credentialsId: 'cbdchang-github'
      }
    }
  }
}
