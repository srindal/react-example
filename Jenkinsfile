pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'npm install'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            bat 'npm run validate'
          }
        }
        stage('error') {
          steps {
            echo 'Hello from parallel'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        bat 'npm run dev'
      }
    }
  }
}