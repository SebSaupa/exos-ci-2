pipeline {
  agent {
    docker { image 'node:14-alpine' }
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