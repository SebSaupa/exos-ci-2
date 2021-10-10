pipeline {
  agent {
    any { image 'node:14-alpine' }
  }
  
  environment{
    STAGING_DOMAIN = 'aloura-staging.surge.sh'
  }

  stages {
    stage('Build') {
      steps {
        sh 'node --version'
        sh 'npm install'
        sh 'npm run build'
      }
    }
    
    stage('deploy to staging (surge)') {
      steps {
        sh 'npm install -y -g surge'
        sh 'surge --project public --domain ${STAGING_DOMAIN}'
      }
    }
  }
}