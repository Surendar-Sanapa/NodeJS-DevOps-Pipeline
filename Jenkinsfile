pipeline {
  agent any

  stages {
    stage('Build Docker Image') {
      steps {
        // Build Docker image
        sh 'docker build -t node-app .'
      }
    }
}
