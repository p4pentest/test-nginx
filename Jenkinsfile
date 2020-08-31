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
                sh 'docker build --no-cache -t "devsecops/server:nginx" -f nginx/Dockerfile'
                sh 'docker run -d --rm -it -p 8081:80 --name nginx-web "devsecops/server:nginx"'
            }
        }
    }
}
