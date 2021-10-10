pipeline {
  agent {
    any { image 'node:14-alpine' }
  }
  
  stages {
    stage('Build') {
      steps {
        sh 'node --version'
        sh 'npm install'
        sh 'npm run build'
      }
    }
  }
}