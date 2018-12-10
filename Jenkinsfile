pipeline {
  agent any
  stages {
    stage('Code Analysis') {
      steps {
        sh 'mvn clean; infer -- mvn compile'
      }
    }
    stage('testing') {
      steps {
        sh 'mvn test'
      }
    }
    stage('packaging') {
      steps {
        sh 'mvn -Dmaven.test.skip=true package'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo \'pipeline success\''
      }
    }
  }
}