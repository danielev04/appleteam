pipeline {
    agent any
    stages {
        stage('Hello World') {
            steps {
                sh 'echo "hello world" '
            }
        }
        stage('Azure Login') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID'
                    sh 'az resource list'
                    sh 'az logout'
                }
            }
        }
    }
}
