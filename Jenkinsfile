pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'Preparing Apache Struts Demo..'
      }
    }

    stage('Stage 2') {
      steps {
        echo 'Starting the Container..'
        sh 'docker run --rm -d -p 80:8080 andrefernandes86/src-demo-apachestruts'
      }
    }

    stage('Stage 3') {
      steps {
        echo 'Testing..'
        sh 'curl 127.0.0.1:80'
      }
    }

  }
}