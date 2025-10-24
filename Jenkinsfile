pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout([$class: 'GitSCM',
          branches: [[name: '*/main']],
          userRemoteConfigs: [[url: 'https://github.com/ICO-Tech/Nodejs-app.git']]
        ])
      }
    }

    stage('Install') {
      steps {
        sh 'npm install'   // adjust for your project
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

    stage('Build') {
      steps {
        sh 'echo Build complete'
      }
    }
  }
}

