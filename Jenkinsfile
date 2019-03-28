pipeline {
    agent any
    stages {
        stage('Login') {
            steps {
                withCredentials([string(credentialsId: 'UMSI', variable: 'Secre')]) {
                    sh 'echo $Secret>/tmp/aaa'
                    sh 'cat /tmp/aaa'
                }
            }
        }
    }
}
