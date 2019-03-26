pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipal('azure_service_principal')]) {
                    sh 'az keyvault secret show --name test  --vault-name infravault99'
                }
            }
        }
    }
}
