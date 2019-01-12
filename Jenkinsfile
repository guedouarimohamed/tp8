pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gradle build'
        archiveArtifacts 'build/libs/*.jar'
      }
    }
    stage('Mail Notification') {
      steps {
        echo 'hi'
      }
    }
    stage('Code Analysis') {
      parallel {
        stage('Code Analysis') {
          steps {
            echo 'code analysids'
          }
        }
        stage('Test Reporting') {
          steps {
            echo 'test'
          }
        }
      }
    }
    stage('Deployment') {
      steps {
        sh 'uploadArchives'
      }
    }
  }
}