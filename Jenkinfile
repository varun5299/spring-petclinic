pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/varun5299/spring-petclinic', branch: 'main')
        sh './mvnw package'
      }
    }

    stage('Run') {
      steps {
        sh 'java -jar /target/spring-petclinic-*.jar &'
      }
    }

  }
}
