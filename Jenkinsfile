pipeline {
  agent any

  stages {
    stage('Run nuclei') {
      steps {
        script {
          docker.image('projectdiscovery/nuclei:latest').inside {
            sh 'nuclei -target app.py -file -type file'
          }
        }
      }
    }
  }
}
