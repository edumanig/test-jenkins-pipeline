pipeline {
    agent any 
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
              sh '/home/ubuntu/pipeline1.sh'
            }
        }
        stage('Deploy') { 
            steps {
              echo 'deploy hello'
            }
        }
    }
}
