#!/usr/bin/env groovy
pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh mvn clean package
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
