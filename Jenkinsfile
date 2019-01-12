pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        archiveArtifacts 'build/libs/*.jar'
      }
    }
    stage('Deployement') {
      steps {
        bat 'gradle uploadArchives'
      }
    }
  }
}