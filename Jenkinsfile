pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the buildjob'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'mvn package'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}