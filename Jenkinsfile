// Using git without checkout 
pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh 'printenv'
        git branch: 'master', url: 'git@github.com:cbdchang/simple-java-maven-app.git', credentialsId: 'cbdchang-github'
      }
    }
  }
}
