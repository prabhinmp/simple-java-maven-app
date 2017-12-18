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
        sh 'sh \'mvn test\''
      }
    }
  }
  environment {
    JAVA_HOME = '/usr/lib/jvm/java-8-oracle/'
  }
}