pipeline {
  agent any
  stages {
    stage('Parallel execution') {
      parallel {
        stage('hellow world') {
          steps {
            sh 'echo "hello world"'
          }
        }

        stage('') {
          agent {
            docker {
              image 'gradle:6-jdk11'
            }

          }
          steps {
            sh 'ci/build-app.sh'
          }
        }

      }
    }

  }
}