pipeline {
  agent any

  environment {
    IMAGE_NAME = 'emc-nodejs-app:latest'
  }

  stages {
    stage('Checkout Code') {
      steps {
        git branch: 'main', url: 'https://github.com/SuryaVelmurugesan/ci-docker-pipeline.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        sh "docker build -t %IMAGE_NAME% ."
      }
    }

    stage('Show Docker Images') {
      steps {
        sh "docker images"
      }
    }
  }
}
