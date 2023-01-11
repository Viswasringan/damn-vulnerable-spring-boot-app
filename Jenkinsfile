pipeline {
 agent none
  stages {
   stage ('Deploy') {
    agent any
    steps {
     sh 'docker run -d -p 8082:8080 dvsba:latest'
    }
   }
   stage ('DAST Scan') {
    agent any
   steps {
    sh 'docker run -v $(pwd):/zap/wrk/:rw -t owasp/zap2docker-stable zap-baseline.py -t http://10.0.2.15:8082/ -g gen.conf -r testreport.html'
   }
   }
  }
}
