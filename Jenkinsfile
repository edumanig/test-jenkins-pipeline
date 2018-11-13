pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'build hello'
          }
        }
        stage('') {
          steps {
            build(job: 'upgrade_only', propagate: true, quietPeriod: 2, wait: true)
          }
        }
        stage('test email') {
          steps {
            emailext(subject: '$BUILD_TAG', body: '$BUILD_DISPLAY_NAME', to: 'edsel@aviatrix.com')
          }
        }
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
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy hello'
      }
    }
  }
  environment {
    PATH = "/home/ubuntu:/home/local/go/bin:/home/ubuntu/work:$PATH"
  }
}