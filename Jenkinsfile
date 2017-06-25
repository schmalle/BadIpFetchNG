pipeline {
  agent any
  def rtGradle = Artifactory.newGradleBuild()
  rtGradle.tool = "Gradle-2.4"
  
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
