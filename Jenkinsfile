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
    stage('') {
      steps {
        mail(subject: 'Build complered successfully', body: 'Hi Team,  The build is ready for deployment', from: 'prabhin.mp@kpisoft.com', to: 'prabhin.mp@kpisoft.com')
      }
    }
  }
  environment {
    JAVA_HOME = '/usr/lib/jvm/java-8-oracle/'
  }
}