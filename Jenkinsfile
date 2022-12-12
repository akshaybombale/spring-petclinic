
pipeline {
  agent any
  stages {
     stage('Install Maven') {
      steps {
        // Install Maven
        sh 'sudo apt-get install maven'
      }
    }
    stage('Build') {
      steps {
        // Run the Maven build
        sh 'mvn clean package'
      }
    }
    stage('Build Docker Image') {
      steps {
        // Build the Docker image
        sh 'docker build -t shanem/spring-petclinic:latest'
      }
    }
    stage('Run Docker Image') {
      steps {
        // Run the Docker image
        sh 'docker run shanem/spring-petclinic:latest'
      }
    }
  }
}





