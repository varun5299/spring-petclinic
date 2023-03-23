pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw clean install -DskipTests'
      }
    }
    stage('SonarQube analysis') {
      steps {
        withSonarQubeEnv('SonarQube') {
          sh './mvnw sonar:sonar'
        }
      }
    }
    stage('Run') {
      steps {
        sh 'java -jar target/*.jar &'
      }
    }
  }
}
