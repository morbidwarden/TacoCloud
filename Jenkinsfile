pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'savevskii/maven:latest' }
      }
      steps {
        sh 'mvn clean install'
        sh 'mvn package'
        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
      }
    }
  }
}