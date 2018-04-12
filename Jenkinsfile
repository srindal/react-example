pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm validate'
      }
    }
    stage('Deploy') {
      steps {
        sh 'npm run dev'
      }
    }
  }
}