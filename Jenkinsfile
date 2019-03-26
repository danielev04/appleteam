pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipal('azure_service_principal')]) {
                    sh ''
                }
            }
        }
    }
}
