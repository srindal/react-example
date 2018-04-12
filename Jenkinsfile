pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'npm install'
      }
    }
    stage('Test') {
      steps {
        bat 'npm validate'
      }
    }
    stage('Deploy') {
      steps {
        bat 'npm run dev'
      }
    }
  }
}