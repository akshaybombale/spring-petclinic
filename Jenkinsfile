
pipeline {
  agent any
  stages {
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





