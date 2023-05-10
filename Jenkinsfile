pipeline{
    agent any
    parameters{
        string(name: 'NAME', defaultValue: 'ubuntu', description: 'enter your name')
        string(name: 'PASSWORD', defaultValue: 'ubuntu', description: 'enter your password')
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
                echo "${params.NAME}"
                echo "${params.PASSWORD}"
            }    
        }
    }
}
