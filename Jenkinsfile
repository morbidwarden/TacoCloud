pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'maven:3.8.6-adoptopenjdk-17' }
      }
      steps {
        sh 'mvn clean install'
        sh 'mvn package'
        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
      }
    }
  }
}