pipeline{
    agent any
    parameters{
        string defaultValue: 'ubuntu', description: 'enter your name', name: 'name'
        string defaultValue: 'ubuntu', description: 'enter your password', name: 'password'
    }    
    stages{
        stage('SCM Checkout'){
            steps{
                git branch:'main', url: 'https://github.com/sajitkumar/ansible1.git'
            }
        }
        stage('Execute playbook on node2'){
            steps{
                ansiblePlaybook disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'slave.yml'
            }
        }   
        stage('login'){
            steps{
                echo "${params.NAME},${params.PASSWORD}"
            }    
        }
    }
}
