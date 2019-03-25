pipeline {
    agent any
    stages {
        stage('accessVault') {
            steps {
                
                withCredentials([string(credentialsId: 'AzureManagedServiceID')]) {
                    sh 'az keyvault secret show --name test  --vault-name infravault99'
                }
            }
        }
    }
}
