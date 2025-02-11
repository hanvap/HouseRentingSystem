pipeline {
  agent any
  environment {
    NUGET_CERT_REVOCATION_MODE = "offline"
    DOTNET_CLI_HTTP_USE_STREAMS = "true"  // Алтернатива за SSL проблеми
  }
  stages {
    stage('Restore') {
      steps {
        bat 'dotnet restore'
      }
    }
    stage('Build') {
      steps {
        bat 'dotnet build'
      }
    }
  }
}
