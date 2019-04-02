pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'build'
      }
    }
    stage('Test') {
      steps {
        echo 'test'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
    stage('Result') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        sh 'echo \'Test result\''
      }
    }
  }
}