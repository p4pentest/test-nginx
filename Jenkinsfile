pipeline {
    agent any
    stages {
        stage('Nginx Build') {
            steps {
                //sh 'ls -ahl'
                //echo 'Hello'
                sh 'docker build -t nginx-server nginx'
            }
        }
        stage('Nginx Deploy') {
            steps {
                //sh 'ls -ahl'
                //echo 'Hello'
                sh 'docker run -d --rm -it -p 8081:80 --name nginx-web nginx-server:latest'
            }
        }
    }
}
