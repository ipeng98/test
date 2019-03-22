pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/ipeng98/test.git', branch: 'master')
      }
    }
    stage('Test') {
      steps {
        echo 'for test'
      }
    }
    stage('Deploy') {
      steps {
        echo 'for deploy'
      }
    }
    stage('finish') {
      steps {
        echo 'done'
      }
    }
  }
  environment {
    Build = 'build'
    Test = 'test'
    Deploy = 'deploy'
  }
}