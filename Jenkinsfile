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
        stage('upgrade_only') {
          steps {
            build(job: 'upgrade_only', propagate: true, quietPeriod: 2, wait: true)
          }
        }
        stage('test email') {
          steps {
            emailext(subject: '$BUILD_TAG - edsel', body: '$BUILD_DISPLAY_NAME - what number', to: 'edsel@aviatrix.com')
            echo 'println GLOBAL_VAR println env.GLOBAL_VAR'
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