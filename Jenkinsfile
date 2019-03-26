pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([AzureMsiCredential('AzureManagedServiceID')]) {
                    sh ''
                }
            }
        }
    }
}
