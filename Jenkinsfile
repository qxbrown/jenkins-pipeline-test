pipeline {
  agent any

  tools {
    nodejs "nodejs"  // You’ll need to define this tool in Jenkins settings
  }

  stages {
    stage('Install') {
      steps {
        sh 'npm ci'  // cleaner install
      }
    }

    stage('Lint') {
      steps {
        sh 'npm run lint'
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
