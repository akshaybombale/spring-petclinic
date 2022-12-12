#!groovy

pipeline {
  agent any
  stages {
          stage {
                 ('Maven Install') 
           agent
                  {
           maven 'maven:3.5.0'
                  }
          }
    stage('Build') {
      steps {
        // Run the Maven build
        sh 'mvn clean install'
      }
    }
    stage('Build Docker Image') {
      steps {
        // Build the Docker image
        sh 'docker build -t shanem/spring-petclinic:latest .'
      }
    }
    stage('Run Docker Image') {
      steps {
        // Run the Docker image
        sh 'docker run shanem/spring-petclinic:latest .'
      }
    }
  }
}







