pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/schmalle/BadIpFetchNG', branch: 'master')
      }
    }
  }
}