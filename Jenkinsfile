node {
  stages {
      stage ('Checkout') {
       steps{
            git 'https://github.com/Praveenreddy003/bazel.git'
      }
      }
    stage('Bazel build') {
      steps {
        sh '''
        ls
        cd examples/cpp
        bazel build hello-world
        '''
      }
    }
  }
}
