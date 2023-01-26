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
        browserstack-sdk python ./tests/test.py
      }
    }
  }
}
