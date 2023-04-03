pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/varun5299/spring-petclinic', branch: 'main')
        sh './mvnw clean package'
      }
    }
    stage('Sonarqube') {
      steps {
        sh './mvnw clean verify sonar:sonar  -Dsonar.projectKey=bb8b69e8605e252c800aa5e13924b50de4acfdc2  -Dsonar.host.url=http://localhost:9000  -Dsonar.login=bb8b69e8605e252c800aa5e13924b50de4acfdc2'
      }
    }

  }
}
