pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        archiveArtifacts 'build/libs/*.jar'
        bat 'gradle build'
      }
    }
  }
}