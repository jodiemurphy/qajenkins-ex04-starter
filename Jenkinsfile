pipeline {
  agent any
  environment {
    registry = "ex04"
    dockerImage = ""
  }
  stages {
    stage("Docker Build") {
      steps {
        dockerImage = docker.build(registry)
        dockerImage.tag("${env.BUILD_NUMBER}")
      }
    }
    stage("Scan Image") {
      steps {
        sh "echo 'Scan Image...'"
      }
    }
  }
}
