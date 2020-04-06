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
        sh 'docker run --rm -d --name apache-struts -p 80:8080 andrefernandes86/src-demo-apachestruts '
      }
    }

    stage('Stage 3') {
      steps {
        echo 'Testing..'
        sh 'curl 127.0.0.1:8080'
        echo 'Demo Ready!'
      }
    }

    stage('Stage 4') {
      steps {
        echo 'Deleting demo..'
        sleep(unit: 'MINUTES', time: 2)
        sh 'docker kill apache-struts'
      }
    }

  }
}