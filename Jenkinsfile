pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                script {
                    // Restores NuGet packages for the solution/project
                    bat 'dotnet restore'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Builds the project without restoring dependencies
                    bat 'dotnet build --no-restore'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Runs all tests in the solution
                    bat 'dotnet test'
                }
            }
        }
    }
}
