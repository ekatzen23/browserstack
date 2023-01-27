pipeline {
  agent any
  stages {
    stage('setup') {
         steps {
            browserstack(credentialsId: 'f39f01e7-7dd8-4744-92ec-9d8369dfa38f') {
                sh 'python3 -m pip3 install browserstack-sdk'
                sh 'browserstack-sdk setup --username "erikkatzen_8b7pJE" --key "LwBRs3y8eNzM1RGY7gZK"'
                sh 'python3 -m venv env'
                sh 'source env/bin/activate'
                sh 'browserstack-sdk python3 ./tests/test.py'
            }
         }
      }
  }
}
