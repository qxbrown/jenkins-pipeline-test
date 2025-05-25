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
         dir('jenkins-test') {
           sh 'npm test'
        }
      }
    }
    stage('Build') {
      steps {
         dir('jenkins-test') {
          sh 'npm run build'
        }
      }
    }
  }
}
