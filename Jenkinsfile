pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t static-website .'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d -p 8080:80 static-website'
      }
    }
  }
}
