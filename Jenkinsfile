pipeline {
    agent any

    triggers {
        corn {'H/1 * * * *'}
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm start'
            }
        }
    }
}

