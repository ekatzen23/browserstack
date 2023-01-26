pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'git clone -b sdk https://github.com/browserstack/python-selenium-browserstack'
        sh 'cd python-selenium-browserstack'
        sh 'python3 -m venv env'
        sh 'source env/bin/activate'
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('hello') {
      steps {
        sh 'browserstack-sdk python3 ./tests/test.py'
      }
    }
  }
}
