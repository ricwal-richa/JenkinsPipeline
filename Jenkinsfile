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
          environment {
            TestVariable = 'Sometest'
          }
          steps {
            writeFile(file: 'TestLogTxtFile.txt', text: "This is a test log file with ${TestVariable}")
          }
        }

      }
    }

    stage('Deploy') {
      when{
          branch 'master'
        }
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploying app in IIS server'
          }
        }

        stage('Artifact') {
          steps {
            archiveArtifacts 'TestLogTxtFile.txt'
          }
        }

      }
    }

  }
  environment {
    ChromeExecutablePath = '/Users/ricagarw/chromedriver.exe'
  }
}
