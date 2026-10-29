pipeline {
    agent any 

    stages {
        stage('hello') {
            steps {
                echo 'hello world'
            }
        }
        stage('create artifact') {
            steps {
                sh 'echo "hello worldd" > hello.txt'
                sh 'cat hello.txt'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'hello.txt', fingerprint: true
        }
    }
}
