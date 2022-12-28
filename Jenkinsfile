pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/mdrajibkhan/docker-java-jenkinsfile-registry.git', branch: 'main', poll: true)
      }
    }

    stage('Build The Application') {
      steps {
        sh 'mvn clean test'
      }
    }

  }
}