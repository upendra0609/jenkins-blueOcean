pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
              date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test step'
          }
        }

        stage('test parallel') {
          steps {
            echo 'test parallel'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}