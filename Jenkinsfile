pipeline {
  agent any
  stages {
    stage('test mvn') {
      steps {
        sh 'mvn -v'
      }
    }
    stage('build') {
      steps {
        sh 'mvn test'
      }
    }
  }
}