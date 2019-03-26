pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureManagedServiceIdentity('AzureManagedServiceID')]) {
                    sh ''
                }
            }
        }
    }
}
