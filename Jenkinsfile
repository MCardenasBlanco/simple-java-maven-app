  node('master') {
    stage('Build a Maven project') {
      script {
        scmVars = checkout([
          $class: 'GitSCM', branches: [[name: "*/master"]],
          doGenerateSubmoduleConfigurations: false,
          gitTool: 'git-ocp',
          submoduleCfg: [],
          userRemoteConfigs: [[url: "https://github.com/cbdchang/simple-java-maven-app.git"]]
        ])
      }
      sh 'mvn -BskipTests clean compile'
    }
  }
