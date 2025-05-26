pipeline {
  agent any
  tools {
    nodejs 'nodejs'
  }
  stages {
    stage('install') {
      steps{
        dir('jenkins-test') {
          sh 'npm install'
         }
       }

    stage('test') {
      steps {
                dir('jenkins-test') {

        sh 'npm test'
}      }
    }

    stage('build') {
      steps {
         dir('jenkins-test') {
           sh 'npm build'
       }
    }}
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
