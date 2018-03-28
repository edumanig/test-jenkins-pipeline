pipeline {
    agent any 
    environment {
        PATH = "/home/ubuntu:/home/local/go/bin:$PATH"
    }
    stages {
        stage('Build') { 
            steps {
              echo 'build hello'
            }
        }
        stage('Test') { 
            steps {
              echo 'test hello'
            }
        }
        stage('Test2') { 
            steps {
              echo "PATH is: $PATH"
              sh "pipeline1.sh"
            }
        }
        stage('Deploy') { 
            steps {
              echo 'deploy hello'
            }
        }
    }
}
