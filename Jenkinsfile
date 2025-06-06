pipeline {
  agent {
    docker {
      image 'ubuntu:22.04'
    }
  }
  stages {
    stage('Test') {
      steps {
        sh 'echo "Running inside Ubuntu container"'
      }
    }
  }
}
