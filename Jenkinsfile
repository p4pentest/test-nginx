pipeline {
    agent any
    stages {
        stage('Nginx Build') {
            steps {
                sh 'docker build -t nginx'
            }
        }
    }
}
