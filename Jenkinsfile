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

    stage('Run Semgrep') {
      steps {
        sh '''
            docker run --rm -v $PWD:/src returntocorp/semgrep semgrep --config=auto --json --output=/src/reports/semgrep/report.json
        '''
      }
    }
  }
}
