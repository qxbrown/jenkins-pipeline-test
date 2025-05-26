pipeline {
  agent any
  tools {
    nodejs 'nodejs'
  }
  stages {
    stage('install') {
      step {
        sh 'npm install'
      }
    }

    stage('test') {
      step{
        sh 'npm test'
      }
    }

    stage('build') {
      step{
        sh 'npm build'
      }
    }
  }
  post {
    success {
      mail to: 'riwaj022@gmail.com',
      subject: "Build Success"
      body: "pipeline succeeded!"
    }
    failure {
      mail to: 'riwaj022@gmail.com',
      subject: "Build Failed"
      body: "Something went wrong!"
    }
  }
}
