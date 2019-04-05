agentName = "appleteam"


pipeline {

    agent { label agentName }
   
    stages {
        stage('Login') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh 'az login --identity '
                }
            }
        }
        stage('Resource Creation') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh 'az storage account create --name apple$(date +%s) --resource-group rg_apple --sku Standard_LRS --location westeurope'
                }
            }
        }
        stage('List Resources') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh 'az resource list | jq ".[].name"'
                }
            }
        }
        stage('Logout') {
            steps {
                withCredentials([azureServicePrincipal('AzureServicePrincipal')]) {
                    sh 'az logout'
                }
            }
        }
    }   
}
