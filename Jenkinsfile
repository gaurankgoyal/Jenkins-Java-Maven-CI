pipeline {
  agent any
  environment {
    USER_NAME = "Joe"
    USER_ID = 42
  }
  stages {
    stage("List env vars") {
      steps {
        sh "printenv | sort"
      }
    }
  stage("using env variable") {
    steps {
      echo "BUILD_NUMBER = ${env.BUILD_NUMBER}"
      sh 'echo BUILD_NUMBER = $BUILD_NUMBER'

      echo "current user is ${env.USER_NAME}"
      echo "current user id ${env.USER_ID} (type: ${env.USER_ID.class})"
    }
  }
  }
  post {
    always {
      cleanWs()
    }
  }
}
