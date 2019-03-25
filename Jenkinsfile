pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipa('AzureServicePrincipal')]) {
                    sh ''
                }
            }
        }
    }
}
