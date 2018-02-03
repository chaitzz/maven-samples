pipeline {
  agent any
  
  /**options {
    buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '2'))
  }*/
  stages {
    /**
    stage('Unit Tests')
      steps {
        sh 'mvn test'
        junit 'reports/results.xml'
      }
    */
    stage('build') {
      steps {
          sh 'mvn package'
      }
    }
    /**
    stage('deploy')
      steps {
        sh 'mvn deploy'
        
      
      }
    
    */
  }
  post {
    always {
      archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
  }
}
