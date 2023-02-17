pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -la'
            git(url: 'https://github.com/Nettune057/Pipeline-CI-CD', branch: 'master')
          }
        }

        stage('version test') {
          steps {
            sh 'python --version'
          }
        }

      }
    }

  }
}