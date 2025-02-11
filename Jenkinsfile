pipeline {  
    agent {  
        docker {  
            image 'mcr.microsoft.com/dotnet/sdk:6.0'  // Заменете с желаната версия на .NET SDK  
        }  
    }  

    stages {  
        stage('Restore') {  
            steps {  
                script {  
                    bat 'dotnet restore'  
                }  
            }  
        }  
        stage('Build') {  
            steps {  
                script {  
                    bat 'dotnet build --no-restore'  
                }  
            }  
        }  
        stage('Test') {  
            steps {  
                script {  
                    bat 'dotnet test'  
                }  
            }  
        }  
    }  
}
