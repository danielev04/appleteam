pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([string(credentialsId: 'UMSI', variable: 'Secret')]) {
                    sh 'echo $Secret'
                }
            }
        }
    }
}
