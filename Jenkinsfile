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

        stage('frontendtest') {
          steps {
            sh '''python3 -version
'''
          }
        }

      }
    }

    stage('build') {
      steps {
        sh '''docker build -f curriculum-front/Dockerfile . -t fuze365/curriculum-front
'''
      }
    }

  }
}