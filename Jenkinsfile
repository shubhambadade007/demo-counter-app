pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                script{
                    
                    git branch: 'main', url: 'https://github.com/shubhambadade007/demo-counter-app.git'
                }
            }
            stage("unit testing"){
                steps{
                    sh 'mvn test'
                }
            }
        
    }
        
}
