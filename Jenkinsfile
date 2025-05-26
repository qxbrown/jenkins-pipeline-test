pipeline {
  agent any
  tools {
    nodejs 'nodejs'
  }
  stages {
    stage('install') {
      steps {
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        sh 'npm test'
      }
    }

    stage('build') {
      steps {
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
