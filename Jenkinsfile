pipeline {
    agent any
    stages {
        stage('accessVault') {
            steps {
                withCredentials([azureServicePrincipal('AzureManagedServiceID')]) {
                    sh 'az keyvault secret show --name test  --vault-name infravault99'
                }
            }
        }
    }
}
