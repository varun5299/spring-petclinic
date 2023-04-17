pipeline {
  agent any
  stages { 
      stage('Execute Ansible') {
            steps {
                ansiblePlaybook credentialsId: 'password', disableHostKeyChecking: true, installation: 'ansible', inventory: '/home/vagrant/dev.inv', playbook: '/home/vagrant/ansible-playbook.yml'
            }
        }
  }
}
