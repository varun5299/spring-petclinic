pipeline {
  agent any
  stages { 
      stage('Execute Ansible') {
            steps {
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: '/home/vagrant/dev.inv', playbook: '/home/vagrant/ansible-playbook.yml'
            }
        }
  }
}
