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
        sh 'mvn clean package'
      }
    }

    stage('Building Docker Images') {
      steps {
        sh 'docker build -t mdrajibkhan/myimage:v1 .'
      }
    }

  }
}