pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o shriyans pes1g19cs117.cpp'
        build job : 'PES1UG19CS117-1'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './shriyans'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying"'
        echo 'Deployment successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
