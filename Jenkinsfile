pipeline {
  agent { label 'master' }
  tools {
    maven 'M3'
  }
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/bhaskaranp/myProject.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
         sh 'mvn test'
         junit '**/target/surefire-reports/TEST-*.xml'
      }
    }   
  }
}