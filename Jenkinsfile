pipeline{
    
    agent any 
     environment {
        PATH = "$PATH:/opt/maven/apache-maven-3.8.6/bin"
    }
    
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
                script{
             
                    
                    sh 'mvn test'
                }
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
