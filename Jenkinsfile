pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipal('AzureManagedServiceID')]) {
                    sh ''
                }
            }
        }
    }
}
