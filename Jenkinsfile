pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building..'
          }
        }
        stage('error') {
          steps {
            echo 'This is nice!'
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
    stage('Keep cool') {
      steps {
        tool 'vscode'
        archiveArtifacts '*.zip'
      }
    }
  }
  environment {
    DUDE = 'Hallo'
  }
}