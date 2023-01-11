pipeline {
 agent none
  stages {
    stage ('Docker Build') {
      agent any
      steps {
        sh 'docker build -t dvsba:latest .'
        sh 'docker run -p -d 8082:8080 dvsba:latest'
      }
    }
   stage ('DAST Scan') {
    agent any
   steps {
    sh 'docker run -t owasp/zap2docker-stable zap-baseline.py -t http://10.0.2.15:8082'
   }
   }
  }
}
