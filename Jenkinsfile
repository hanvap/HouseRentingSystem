pipeline {
  agent any
  environment {
    NUGET_CERT_REVOCATION_MODE = "offline"
    DOTNET_CLI_HTTP_USE_STREAMS = "true"  // Алтернативно решение за SSL проблеми
  }
  stages {
    stage('Restore') {
      steps {
        bat 'dotnet restore --interactive'  # --interactive може да помогне при прокси
      }
    }
    stage('Build') {
      steps {
        bat 'dotnet build'
      }
    }
    stage('Test') {
      steps {
        bat 'dotnet test'
      }
    }
  }
}
