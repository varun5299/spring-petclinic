pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/varun5299/spring-petclinic', branch: 'main')
        sh './mvnw clean package'
      }
    }
      stage('Execute Ansible') {
            steps {
                ansiblePlaybook credentialsId: 'password', disableHostKeyChecking: true, installation: 'ansible', inventory: '/home/vagrant/dev.inv', playbook: '/home/vagrant/ansible-playbook.yml'
            }
        }
  }
}
