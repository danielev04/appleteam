agentName = "appleteam"


pipeline {

    agent { label agentName }
   
    stages {
        stage('Login') {
            steps {
                sh 'az login --identity '
            }
        }
        stage('Resource Creation') {
            steps {
                sh 'az storage account create --name apple$(date +%s) --resource-group rg_apple --sku Standard_LRS --location westeurope'
            }
        }
        stage('List Resources') {
            steps {
                sh 'az resource list | jq ".[].name"'
            }
        }
        stage('Logout') {
            steps {
                sh 'az logout'
            }
        }
    }   
}
