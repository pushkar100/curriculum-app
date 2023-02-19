pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/pushkar100/curriculum-app', branch: 'dev')
      }
    }

    stage('List files') {
      parallel {
        stage('List files') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Frontend unit test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}