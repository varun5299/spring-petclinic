pipeline {
  agent any
  stages { 
    stage('Deploy'){         
      steps{
        ansiblePlaybook( 
          playbook: '/home/vagrant/ansible-playbook.yml',
          inventory: '/etc/ansible/hosts', 
          )
            }
        }
  }
}
