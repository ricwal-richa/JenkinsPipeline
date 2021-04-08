pipeline{
    agent{
        dockerfile {
            dir 'build'
        }
    }
    stages{
        stage('Build'){
          steps{
                sh 'node --version'
                sh 'pwd'
          }
        }
    } 
}
