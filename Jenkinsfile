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
        sh 'mvn test -B'
      }
    }
    stage('install') {
      steps {
        sh 'mvn install'
      }
    }
    stage('cleaninstall') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
  environment {
    JAVA_HOME = '/usr/lib/jvm/java-8-oracle/'
  }
}