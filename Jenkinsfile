pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                script{
                    
                    git branch: 'main', url: 'https://github.com/shubhambadade007/demo-counter-app.git'
                }
            }
        }
        stage('UNIT testing'){
            
            steps{
             
                    
                    sh 'mvn test'
                
            }
        }
         stage('Integration testing'){
            
            steps{
                
                script{
                    
                    sh 'mvn verify -DskipUnitTests'
                }
            }
        }
    }
}
