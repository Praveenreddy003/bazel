pipeline {
  agent any
  stages {
      stage ('Checkout') {
       steps{
            checkout scm 
      }
      }
    stage('Publish image') {
      steps {
        sh 'bazel build hello-word'
      }
    }
  }
}
