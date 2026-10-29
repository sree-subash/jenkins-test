pipeline {
  agent any
  stages {
    stage('hello') {
      steps {
        echo 'hello world'
          }
        }
    stage('build') {
      steps {
        sh 'echo "build completed"'
      }
    }
  }
}
post {
  succuss {
    archiveArtifacts artifacts: 'hello.txt', fingerprint: true
  }
}
}
