pipeline {
   agent any
    stages {
      stage('Build') {
         steps {
            sh 'docker build . -t getintodevops-hellonode:1'
         }
      }
      stage('Deploy') {
         steps {
                  sh 'docker run -it -p 80:80 getintodevops-hellonode:1'
         }
      }
