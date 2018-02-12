pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'I am building.'
            sh '''javac Hello.java
java Hello'''
          }
        }
        stage('sonar') {
          steps {
            echo 'I am sonar scan'
          }
        }
        stage('fortify') {
          steps {
            echo 'I am fortify scan'
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'I am testing now'
      }
    }
    stage('integrate') {
      steps {
        echo 'integrating now'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying now'
      }
    }
  }
}