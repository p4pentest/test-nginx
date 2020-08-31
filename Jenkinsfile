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
                sh 'docker build --no-cache -t nginx-web nginx'
                sh 'docker run -d --rm -it -p 8081:80 --name nginx-w nginx-web'
            }
        }
    }
}
