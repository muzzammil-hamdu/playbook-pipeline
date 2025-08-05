pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                  git branch: 'main' , url: 'https://github.com/muzzammil-hamdu/playbook-pipeline.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                  sh 'ansible-playbook -i inventory.ini create_file.yml'
            }
        }
    }
}
