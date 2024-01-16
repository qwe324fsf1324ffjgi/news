pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/qwe324fsf1324ffjgi/news', branch: 'master')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

    stage('Log into Dockerhub') {
      environment {
        DOCKERHUB_USER = 'fuze365'
        DOCKERHUB_PASSWORD = 'gv1&3Ea9W##onDQAMUG&41CvZ7h1d1'
      }
      steps {
        sh 'docker login -u zerah550 -p Zee6oi41ife'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push zerah550/curriculum-front:latest'
      }
    }

  }
}