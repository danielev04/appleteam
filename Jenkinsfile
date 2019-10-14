agentName = "appleteam"


pipeline {

    //agent { label agentName }
    
    agent any
    
    parameters {
        choice(name: 'A', choices: ['yes', 'no'], description: 'description')
    }
    
    environment {
        varA = "myvar"
    }
    
    options {
    }
    stages {
        /*
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
        }*/
        stage('stage 1') {
            steps {
                echo "description"
                
                script {
                    if (param.A == 'yes'){
                       sh """
                        echo 'yes'
                        """
                    }
                }
                sh """
                    echo ${env.varA}
                """
                
            }
        }
    }   
}
