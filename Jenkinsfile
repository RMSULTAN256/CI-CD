pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        checkout scm
      }
    }

    stage('installing') {
      steps {
        sh '''
            if ! command -v semgrep >/dev/null; then
              pip3 install semgrep --user
        '''
      }
    }
  }
}
