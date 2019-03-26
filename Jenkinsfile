pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([AzureMsiCredentials('AzureManagedServiceID')]) {
                    sh ''
                }
            }
        }
    }
}
