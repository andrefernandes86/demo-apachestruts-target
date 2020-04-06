pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'Phase 1'
      }
    }

    stage('Stage 2') {
      steps {
        echo 'Phase2'
        sh 'docker run --rm -d -p 80:8080 andrefernandes86/src-demo-apachestruts:latest'
      }
    }

  }
}