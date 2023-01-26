pipeline {
  agent any
  stages {
    stage('setup') {
         steps {
            browserstack(credentialsId: 'f39f01e7-7dd8-4744-92ec-9d8369dfa38f', localConfig: [localOptions: '<local-options>', localPath: '/path/to/local']) {
                // For macOS-based systems, add the following commands in the given console to download the binary, run it, and stop its execution after the test has been executed.
                sh 'wget "https://www.browserstack.com/browserstack-local/BrowserStackLocal-darwin-x64.zip"'
                sh 'unzip BrowserStackLocal-darwin-x64.zip'
                sh './BrowserStackLocal --key $LwBRs3y8eNzM1RGY7gZK --daemon start'
                sh 'browserstack-sdk python3 ./tests/test.py'
                sh './BrowserStackLocal --key $LwBRs3y8eNzM1RGY7gZK --daemon stop' 
            }
            browserStackReportPublisher 'automate'
         }
      }
  }
}
