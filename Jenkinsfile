pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date
ls
'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'this is second stage'
          }
        }

        stage('test pro') {
          steps {
            echo 'this is the producton test'
          }
        }

        stage('test deploy') {
          steps {
            echo 'this is deploy'
          }
        }

      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'this is deploy stage'
          }
        }

        stage('sleep') {
          steps {
            sleep 20
          }
        }

      }
    }

  }
}