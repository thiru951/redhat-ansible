pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/thiru951/redhat-ansible.git'
            }
        }

        stage('Run Ansible') {
            steps {
                sh '''
                ansible-playbook -i inventory.yml patch.yml
                '''
            }
        }
    }
}
