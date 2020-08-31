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
        stage('Nginx Deploy') {
            steps {
                //sh 'ls -ahl'
                //echo 'Hello'
                sh 'docker run --rm -t -p 8081:80 nginx'
            }
        }
    }
}
