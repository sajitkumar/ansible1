pipeline {
    agent any
            
   stages{
        stage('scm checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/sajitkumar/ansible1.git'
                
            }
        }
        stage('execute playbook'){
            steps{
                ansiblePlaybook credentialsId: 'ansible1', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'ngin.yml'
                
            } 
        }
    }
} 
