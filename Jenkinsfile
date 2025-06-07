pipeline {
  agent any

  stages {
    stage('Run nuclei') {
      steps {
        script {
          sh 'semgrep ci'
        }
      }
    }
  }
}
