pipeline {
  agent any

  stages {
    stage('Requirements') {
      steps {
        sh 'chmod +x ./algorithm.sh'
      }
    }
    stage('Build') {
      steps {
        sh './algorithm.sh'
        archiveArtifacts artifacts: '*.txt', followSymlinks: false, onlyIfSuccessful: true
      }
    }
  }
}
