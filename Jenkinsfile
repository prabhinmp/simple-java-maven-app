pipeline {
  agent any
  stages {
    stage('clean') {
      steps {
        sh '''#!/bin/bash
mvn clean install'''
      }
    }
  }
}