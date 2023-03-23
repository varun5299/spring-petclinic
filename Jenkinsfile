pipeline {
  agent any
  stages {
    stage('SonarQube') {
      steps {
        withSonarQubeEnv(installationName: 'sonarqube', credentialsId: 'sonarCredentials') {
          sh './mvnw clean verify sonar:sonar'
        }
      }
    }
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }
  }
}
