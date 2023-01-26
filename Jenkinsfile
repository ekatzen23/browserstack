pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'browserstack-sdk python3 ./tests/test.py'
      }
    }
  }
}
