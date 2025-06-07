pipeline {
  agent any

  environment {
    PATH = "${env.HOME}/.local/bin:${env.PATH}"
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Install Semgrep') {
      steps {
        sh '''
          if ! command -v semgrep >/dev/null; then
            pip3 install semgrep --user
          fi

          which semgrep
        '''
      }
    }

    stage('Run Semgrep') {
      steps {
        sh '''
          semgrep --config=auto --json --output=reports/semgrep/report.json
        '''
      }
    }
  }
}
