pipeline {
 agent none
  stages {
   stage ('DAST Scan') {
    agent any
   steps {
    sh 'docker run -t owasp/zap2docker-stable zap-baseline.py -t http://10.0.2.15:8082/ ||true'
   }
   }
  }
}
