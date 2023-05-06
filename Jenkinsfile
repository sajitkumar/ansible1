pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch:'main' url: 'https://github.com/sajitkumar/ansible1.git,
            }
        }
        stage('Execute Ansible'){
            steps{
                ansiblePlaybook credentialsId: 'ansible', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'nginx.yml'
            }
        }
    }
}
