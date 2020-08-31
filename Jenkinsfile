pipeline {
    agent none
    stages {
        stage('Test') {
            agent {
                docker {
                image 'node:7-alpine'
                args '--name docker-node' // list any args
                }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
