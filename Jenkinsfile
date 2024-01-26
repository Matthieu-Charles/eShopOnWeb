pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'dotnet build eShopOnWeb.sln'
      }
    }

    stage('Functional') {
      steps {
        sh 'dotnet test tests/FunctionalTests'
      }
    }

    stage('Deployment') {
      steps {
        sh 'dotnet publish eShopOnWeb.sln -0 /var/aspnet'
      }
    }

  }
}