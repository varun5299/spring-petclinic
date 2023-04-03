pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/varun5299/spring-petclinic', branch: 'main')
        sh 'mvn package'
      }
    }

    stage('spring run') {
      steps {
        sh 'java -jar /target/spring-petclinic-2.6.0-SNAPSHOT.jar &'
      }
    }

  }
}


