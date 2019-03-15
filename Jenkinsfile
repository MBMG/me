pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Build script') {
      steps {
        sh 'npm run build'
      }
    }
  }
}