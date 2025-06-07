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
            if ! command -v python3 >/dev/null: then
                sudo apt-get update && sudo apt-get install -y python3 python3-pip
            fi

            if ! command -v semgrep >/dev/null; then
              pip3 install semgrep --user
              export PATH=$OATH:$HOME/.local/bin
            fi

            which semgrep || echo "Semgrep not in PATH"
        '''
      }
    }
  }
}
