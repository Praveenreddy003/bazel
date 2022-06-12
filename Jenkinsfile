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

post {
    success {
      sh "echo 'Send mail on success'"
      // mail to:"madupupraveen003@gmail.com", subject:"SUCCESS: ${currentBuild.fullDisplayName}", body: "Yay, we passed."
    }
    failure {
      sh "echo 'Send mail on failure'"
      // mail to:"madupupraveen003@gmail.com", subject:"FAILURE: ${currentBuild.fullDisplayName}", body: "Boo, we failed."
    }
  }
