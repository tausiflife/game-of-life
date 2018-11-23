#!/usr/bin/env groovy
pipeline {
  agent any
  tools {
    maven 'maven3'
    jdk 'jdk1.8'
  }
  parameters {
    string(name: 'greeting', defaultValue: 'hello', description: 'How should i greet world?')
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
    stage('Give input'){
      steps {
        script {
             def userInput = input(id: 'userInput', message: 'Merge to?',
             parameters: [[$class: 'ChoiceParameterDefinition', defaultValue: 'strDef', 
                description:'describing choices', name:'nameChoice', choices: "QA\nUAT\nProduction\nDevelop\nMaster\n${params.greeting}"]
             ])

            println(userInput); //Use this value to branch to different logic if needed
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}
