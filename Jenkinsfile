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
            echo "The path for Chromedriver is ${ChromeExecutablePath}"
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
  environment {
    ChromeExecutablePath = '/Users/ricagarw/chromedriver.exe'
  }
}