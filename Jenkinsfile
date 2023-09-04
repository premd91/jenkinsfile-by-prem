pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test to deploy'
          }
        }

        stage('test parameter') {
          steps {
            echo 'test para should be done'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy to prod'
        sleep 10
      }
    }

  }
}