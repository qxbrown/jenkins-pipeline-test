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
    mail to: 'you@example.com',
         subject: "Build Success: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
         body: "Pipeline succeeded!"
  }
  failure {
    mail to: 'you@example.com',
         subject: "Build Failed: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
         body: "Something went wrong."
  }
}

}
