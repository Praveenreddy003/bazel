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
        sh '/var/lib/jenkins/workspace/Bazel pipeline/examples/cpp;bazel build hello-world'
      }
    }
  }
}
