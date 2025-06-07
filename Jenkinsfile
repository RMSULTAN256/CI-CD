pipeline {
  agent any

  stages {
    stage('Run nuclei') {
      steps {
        script {
          sh 'nuclei -target app.py -file -type file -json -o report.json'
        }
      }
    }
  }
}
