pipeline {
  agent any
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
    }
  }
  }
  post {
    always {
      cleanWs()
    }
  }
}
