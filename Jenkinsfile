pipeline {
  agent any
  tools {
    nodejs 'nodejs'
  }
  stages {
    stage('install') {
      steps{
        dir('next_node_jenkins') {
          sh 'npm install'
         }
       }
}
    stage('test') {
      steps {
                dir('next_node_jenkins') {

        sh 'npm test'
}      }
    }

    stage('build') {
      steps {
         dir('next_node_jenkins') {
           sh 'npm run build'
       }
    }}
  }

}
