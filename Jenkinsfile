pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([AzureBaseCredentials('AzureManagedServiceID')]) {
                    sh ''
                }
            }
        }
    }
}
