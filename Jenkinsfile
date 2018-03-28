pipeline {
    agent any 
    environment {
        PATH = "/home/ubuntu:/home/local/go/bin:/home/ubuntu/work:$PATH"
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
              version = readMavenPom.getVersion()
              echo "PATH is: $PATH"
              #sh "pipeline1.sh"
            }
        }
        stage('Deploy') { 
            steps {
              echo 'deploy hello'
            }
        }
    }
}
