pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh ''
                }
            }
        }
    }
}
