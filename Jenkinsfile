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

        stage('Test Log') {
          steps {
            writeFile(file: 'TestLogTxtFile.txt', text: 'This is a test log file')
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