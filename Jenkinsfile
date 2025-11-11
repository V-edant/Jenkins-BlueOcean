pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date
ls'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This is Test-Step'
          }
        }

        stage('Test-PAR') {
          steps {
            echo 'Test_PAR'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'This is the deployment Activity'
        sleep 15
      }
    }

  }
}