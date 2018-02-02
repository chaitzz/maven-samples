pipeline {
  agent any

  stages {
    stage('build') {
      steps {
          sh 'mvn package'
      }
    }
  }
  post {
    always {
      archiveArtifacts: 'target/*.jar', fingerprint: true
    }
  }
}
