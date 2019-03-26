pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                    sh 'az login --identity'
                    sh 'az keyvault secret show --name test  --vault-name infravault99'
               
            }
        }
    }
}
