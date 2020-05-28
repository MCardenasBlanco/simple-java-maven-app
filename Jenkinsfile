// Using git without checkout 
pipeline {
  agent any
  environment {
    GIT_SSH_COMMAND='ssh -vvv'
    GIT_CURL_VERBOSE=1
    GIT_TRACE=1
  }
  tools {
    git 'git-ocp'
  }
  stages {
    stage('Checkout') {
      steps {
        sh 'printenv'
        // git branch: 'master', url: 'git@github.com:cbdchang/simple-java-maven-app.git', credentialsId: 'cbdchang-github'
        checkout([
            $class: 'GitSCM', branches: [[name: "*/master"]],
            doGenerateSubmoduleConfigurations: false,
            gitTool: 'git-ocp',
            submoduleCfg: [],
            userRemoteConfigs: [[credentials: 'cbdchang-github', url: "https://github.com/cbdchang/simple-java-maven-app.git"]]])
      }
    }
  }
}
