pipeline {
  agent any

  stages {
    stage("Build") {
      steps {
      }
    }

    stage("Testing") {
      parallel {
        stage("Unit Tests") {
          agent { docker 'openjdk:11-jdk-alpine' }
          steps {
            sh 'java -version'
          }
        }
        stage("Functional Tests") {
          agent { docker 'openjdk:11-jdk-alpine' }
          steps {
            sh 'java -version'
          }
        }
        stage("Integration Tests") {
          steps {
            sh 'java -version'
          }
        }
      }
    }

    stage("Deploy") {
      steps {
        echo "Deploy!"
      }
    }
  }
}