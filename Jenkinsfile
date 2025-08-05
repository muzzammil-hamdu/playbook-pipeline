pipeline {
    agent any
    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/muzzammil-hamdu/playbook-pipeline.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                sshagent(['vm1-key']) {
                    sh 'ansible-playbook -i inventory.ini create_file.yml'
                }
            }
        }
    }
}
