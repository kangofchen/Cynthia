pipeline {
  agent any
  stages {
    stage('Print') {
      parallel {
        stage('Print') {
          steps {
            echo 'Test a message'
          }
        }
        stage('sleep test') {
          steps {
            sleep 5
          }
        }
      }
    }
    stage('shell') {
      steps {
        sh 'echo \'shell is here\''
      }
    }
    stage('mail') {
      parallel {
        stage('mail') {
          steps {
            echo 'send a mail'
          }
        }
        stage('auto test') {
          steps {
            echo 'to exe auto test'
          }
        }
      }
    }
    stage('gitlab') {
      steps {
        echo 'exe webhook of gitlab'
      }
    }
    stage('intergeration') {
      steps {
        echo 'intergeration test success'
      }
    }
  }
}