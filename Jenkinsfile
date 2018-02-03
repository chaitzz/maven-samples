pipeline {
  agent any
  
  /**options {
    buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '2'))
  }*/
  stages {
    stage('build') {
      steps {
          sh 'mvn package'
      }
    }
  }
  post {
    always {
      archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
  }
}
