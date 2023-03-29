pipeline{

    agent any

    stages{
        
        agent{
            docker{
                image 'maven'
            }
        }
        stage('sonar quality status'){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh 'maven clean package sonar:sonar'
                    }
                }

            }

       }

   }  
    
}