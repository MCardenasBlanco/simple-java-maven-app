pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Echo environment') {
            steps {
                sh 'printenv'
            }
        }
    }
}
