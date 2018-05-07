pipeline {
  agent { label 'master' }
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