pipeline {
  agent any
  stages {
      stage ('Checkout') {
       steps{
            checkout scm 
      }
      }
    stage('Bezel build') {
      steps {
        sh "cd /var/lib/jenkins/workspace/Bazel pipeline/examples/cpp;bazel build hello-world"
      }
    }
  }
}
