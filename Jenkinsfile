pipeline{
    agent any
    
    stages{
        stage("Restore .Net Packages"){
            steps{
                bat 'dotnet restore' //For Windows
                
              }
           
        }
        stage("Build.Net Project"){
                bat 'dotnet build --no restore' //For Windows
              }

        stage("Run Unit and Integration Test"){
            steps{
                bat 'dotnet test -- no-build --verbosity normal' // For Windows
            }
        }   
    }
   
}