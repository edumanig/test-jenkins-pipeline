pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'hello'
      }
    }
  stages {
    stage('Test') {
       steps {
         cd /home/ubuntu
         sh "jenkins_terraform_install.sh"
         sh ""/usr/local/go/bin/go version"

        }
    }
  }
}