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
      archive 'target/*.jar'
    }
  }
}
