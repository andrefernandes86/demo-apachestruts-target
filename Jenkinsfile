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
        sleep 10
        sh 'curl 192.168.1.84'
        echo 'Demo Ready!'
      }
    }

    stage('Stage 4') {
      steps {
        echo 'Deleting demo..'
        sleep(unit: 'HOURS', time: 1)
        sh 'docker kill apache-struts'
      }
    }

  }
}