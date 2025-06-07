pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
  }

  stages {
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
