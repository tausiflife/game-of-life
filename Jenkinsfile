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
        sh '''
           echo "PATH = ${PATH}"
           echo "M2_HOME = ${M2_HOME}"
           '''
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
