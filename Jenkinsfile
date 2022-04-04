pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        git(url: 'https://github.com/Fred0086/JavaJunitWar.git', branch: '*/master')
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('test') {
      steps {
        junit 'target/surefire-reports/TEST-*.xml'
      }
    }

  }
}