pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Nettune057/Pipeline-CI-CD', branch: 'master')
      }
    }

    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -la'
          }
        }

        stage('version test') {
          steps {
            sh 'python3 --version'
          }
        }

      }
    }

    stage('build') {
      steps {
        sh '''docker build -f python/Dockerfile . 
'''
      }
    }

  }
}