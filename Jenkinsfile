pipeline{
    agent any
    parameters{
        choice(name: 'branch', choices: ['main'], description: ' ')
    }    
    stages{
         stage('SCM Checkout'){
             when{
                 expression{
                     params.branch == "main"
                 }
             }    
            steps{
                git branch:'main', url: 'https://github.com/sajitkumar/ansible1.git'
            }
         }
    }
}
