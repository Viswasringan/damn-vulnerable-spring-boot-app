pipeline {
 agent none
  stages {
   stage ('SAST Scan') {
    steps {
     withSonarQubeEnv('sonar'){
     sh 'mvn sonar:sonar'
     sh 'cat $(pwd)/sonar/report-task.txt '
     }
     
    }
   }
   /*stage ('Deploy') {
    agent any
    steps {
     sh 'docker run -d --name dvsba -p 8082:8080 dvsba:latest'
    }
   }
   stage ('DAST Scan') {
    agent any
   steps {
    sh 'docker run -v /home/ubuntu:/zap/wrk/:rw --name zapscan -t owasp/zap2docker-stable zap-baseline.py -t http://10.0.2.15:8082/ -g gen.conf -r testreport.html ||true'
    sh 'docker rm zapscan'
    sh 'docker stop dvsba'
    sh 'docker rm dvsba'
   }
   }*/
  }
}
