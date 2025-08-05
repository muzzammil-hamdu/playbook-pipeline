pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                  git url: 'https://github.com/muzzammil-hamdu/playbook-pipeline.git', branch: 'main'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                  sh 'ansible-playbook -i inventory.ini create_file.yml'
            }
        }
    }
}
