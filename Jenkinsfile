pipeline {
  agent any
  stages {
    stage('setup') {
         steps {
            browserstack(credentialsId: 'f39f01e7-7dd8-4744-92ec-9d8369dfa38f') {
                sh 'browserstack-sdk python3 ./tests/test.py'
            }
         }
      }
  }
}
