#!/usr/bin/env groovy
pipeline {
  agent any
  tools {
    maven 'maven3'
    jdk 'jdk1.8'
  }
  stages {
    stage('Initialize') {
      steps {
        echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
      }
    }
    stage('Build') {
      steps {
        echo 'building'
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
