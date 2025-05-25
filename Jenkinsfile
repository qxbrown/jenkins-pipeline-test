pipeline {
  agent any

  tools {
    nodejs "nodejs"
  }

  stages {
    stage('Install') {
      steps {
        dir('jenkins-test') {
          sh 'npm install'
        }
      }
    }
   stage('Lint') {
    steps {
        echo 'Skipping lint for now'
        // sh 'npm run lint'
    }
}
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
  }
}
