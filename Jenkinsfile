pipeline {
  agent any
  stages { 
    stage('Deploy'){         
      steps{
        ansiblePlaybook( 
          inventory: '/etc/ansible/hosts',
          playbook: '/home/vagrant/ansible-playbook.yml', 
          )
            }
        }
  }
}
