pipeline {
  agent any

  stages {
    stage('build') {
      steps {
          sh 'mvn compile'
      }
    }
  }
  post {
    always {
      archive 'target/*.jar'
    }
  }
}
