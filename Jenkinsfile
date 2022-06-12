pipeline {
  agent any
  stages {
      stage ('Checkout') {
       steps{
            checkout scm 
      }
      }
    stage('Bazel build') {
      steps {
        sh "cd /var/lib/jenkins/workspace/bazelnewproject/examples/cpp;bazel build hello-world"
      }
    }
  }
}
