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
    stage('test') {
      steps {
        sh 'npm test'
        emailext(subject: 'Prueba jenkins', body: 'Envio desde Jenkins', attachLog: true, to: 'blancamaria')
      }
    }
    stage('Aprove') {
      steps {
        input(message: 'Aprobar?', submitter: 'mariablanca')
      }
    }
    stage('Deploy') {
      steps {
        emailext(subject: 'Prueba correo 2', body: 'Otra prueba desde Jenkins, pase a PROD', attachLog: true, to: 'mariablanca')
      }
    }
  }
}