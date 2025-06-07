pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
  }

  stages {
    stage('Test') {
      steps {
        script {
          docker.image('projectdiscovery/nuclei:latest').inside {
            sh 'nuclei -version'
          }
        }
      }
    }
  }
}
