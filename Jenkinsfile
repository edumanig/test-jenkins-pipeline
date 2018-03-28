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
                #sh './gradlew check'

                cd /home/ubuntu
                sh "jenkins_terraform_install.sh"

                # show go version
                /usr/local/go/bin/go version
            }
        }
    }
  }
}