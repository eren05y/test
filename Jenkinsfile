pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'This is a build stage.'
          }
        }

        stage('') {
          steps {
            sh 'echo "build on mac"'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'This is a test stage.'
      }
    }

    stage('Deploy') {
      steps {
        echo 'This is a deploy stage.'
      }
    }

  }
}