pipeline {
   agent any
    stages {
      stage('Build') {
         steps {
            echo 'Hello..This is build stage!'
            input('Do you want to proceed?')
         }
      }
      stage('Archive') {
         steps {
                  echo 'Hello..This is archive stage!'
                  input('Do you want to proceed?')
         }
      }
      stage('Staging') {
         parallel { 
                  stage('Parallel Stage 1') {
                           steps {
                                echo 'Hello..This is parallel stage 1!'
                                input('Do you want to proceed?')
                           }
                  }
                  stage('Parallel Stage 2') {
                           steps {
                                echo 'Hello..This is parallel stage 2!'
                                 input('Do you want to proceed?')
                           }
                  }
         }
      }
      stage('Deploy') {
         steps {
                  echo 'Hello..This is build stage!'
                  input('Do you want to proceed?')
         }
      }
    }
}
