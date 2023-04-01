pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/varun5299/spring-petclinic', branch: 'main')
      }
    }

    stage('SonarQube analysis') {
      steps {
        withSonarQubeEnv('SonarQube') {
          sh 'mvn sonar:sonar -Dsonar.projectKey=PetClinic -Dsonar.host.url=http://localhost:9000 -Dsonar.login=94d4d50956f55f982d5ec8f27d8b8922646e5fc9'
        }
      }
    }
    
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Execute jar') {
      steps {
        sh 'java -jar target/spring-petclinic-2.4.5.jar'
      }
    }
  }
}

