pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                script {
                    // Restores NuGet packages for the solution/project
                    sh 'dotnet restore'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Builds the project without restoring dependencies
                    sh 'dotnet build --no-restore'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Runs all tests in the solution
                    sh 'dotnet test'
                }
            }
        }
    }
}
