pipeline {
    agent any
    stages {
        stage('Docker Clear') {
            steps {
                sh 'docker images -f dangling=true -q | xargs docker rmi || true'
            }
        }
        stage('Nginx Deploy') {
            steps {
                sh 'docker build --no-cache -t webserver:nginx-web nginx'
                sh 'docker rm nginx-w --force || true'
                sh 'docker run -d --rm -it -p 808:80 --name nginx-w webserver:nginx-web'
            }
        }
    }
}
