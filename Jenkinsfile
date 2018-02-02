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
      archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
  }
}
