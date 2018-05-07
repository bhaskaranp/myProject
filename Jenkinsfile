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
  }
}