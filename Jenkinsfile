pipeline {
    agent any
    stages {
        stage('Nginx Build') {
            steps {
                sh 'docker --build -t nginx'
            }
        }
        stage('Nginx Deploy') {
            steps {
                sh 'docker run --rm -it -p 8081:80 nginx'
            }
        }
    }
}
