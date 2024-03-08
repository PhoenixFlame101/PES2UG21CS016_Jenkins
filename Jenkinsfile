pipeline {
  agent any
  stages {
    stage('Build') {
          steps {
            build 'PES2UG21CS016-1'
            sh 'g++ main.cpp -o hello_world'
          }
          }
          stage('Test') {
            steps {
              sh './hello_world'
            }
          }
          stage('Deploy') {
            steps {
              echo 'deploy'
            }
          }
          }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
