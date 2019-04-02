pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'build'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test'
          }
        }
        stage('') {
          steps {
            sleep 10
          }
        }
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