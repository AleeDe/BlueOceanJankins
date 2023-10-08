pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh '''echo "Hello World"
pwd'''
            sh '''echo "Another Echo"
'''
          }
        }

        stage('error') {
          steps {
            sh 'echo "Testing"'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh '''echo "Building "
'''
      }
    }

    stage('waiting') {
      steps {
        input(message: 'Should we continue', ok: 'Why not')
      }
    }

  }
}