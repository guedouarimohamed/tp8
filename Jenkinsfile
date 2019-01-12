pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        archiveArtifacts 'build/libs/*.jar'
        bat(script: 'gradle uploadArchives', returnStatus: true, returnStdout: true)
      }
    }
  }
}