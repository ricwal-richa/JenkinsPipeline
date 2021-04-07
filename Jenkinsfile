pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Hello Build'
          }
        }

        stage('Test') {
          steps {
            echo 'Hello Test'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying app in IIS server'
      }
    }

  }
}