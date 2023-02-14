pipeline {
  agent any
  stages {
    stage('SSH test') {
      steps {
        sh '''#!/bin/bash

ssh -tt ubuntu@172.17.0.3\'
ls -la
\''''
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

  }
}