#!/usr/bin/env groovy
pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        mvn clean install
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
    }
    stage('Test') {
      steps {
        echo 'Testing'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}
