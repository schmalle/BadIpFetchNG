pipeline {
  agent any
  def rtGradle = Artifactory.newGradleBuild()
  rtGradle.tool = "Gradle 4.0"
  
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/schmalle/BadIpFetchNG', branch: 'master')
      }
    }
    stage('Build') {
              buildInfo = rtGradle.run rootDir: ".", buildFile: 'build.gradle', tasks: 'build'
      
      }
    }
  }
}
