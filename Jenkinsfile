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
            bat 'npm validate'
          }
        }
        stage('') {
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