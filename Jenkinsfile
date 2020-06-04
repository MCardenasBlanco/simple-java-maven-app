podTemplate(label: 'inplace', containers: [
  containerTemplate(name: 'jnlp', image: 'maven:3.6.2-jdk-8-slim', command: 'sh', args: '/var/jenkins_config/jenkins-agent'),
  ], volumes: [
        configMapVolume(mountPath: '/var/jenkins_config', configMapName: 'jenkins-agent')
  ],) {

  node('inplace') {
    stage('Build a Maven project') {
      sh 'ls -l'
      sh 'mvn -BskipTests clean compile'
    }
  }
}
