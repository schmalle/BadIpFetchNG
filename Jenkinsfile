pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/schmalle/BadIpFetchNG', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        sh '''/root/.sdkman/bin/sdkman-init.sh
gradle build
'''
      }
    }
  }
}