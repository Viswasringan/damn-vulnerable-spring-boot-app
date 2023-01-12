pipeline {
 agent any
 stages {
  stage('Secret Scan') {
   steps {
    sh 'sudo docker run zricethezav/gitleaks detect -v -f csv -r gitleaks.csv'
   }
  }
  /*stage('SCM') {
   steps {
    checkout scm
   }
  }
  stage('SonarQube Analysis') {
   steps {
    withSonarQubeEnv('sonar') {
      sh "./gradlew sonarqube"
    }
    }
  }
}*/
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
   } API_TOKEN=123456789 */
 } 
}
