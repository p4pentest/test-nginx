pipeline {
    agent any
    stages {
        stage('Nginx Build') {
            steps {
                //sh 'ls -ahl'
                //echo 'Hello'
                sh 'docker build nginx'
            }
        }
    }
}
