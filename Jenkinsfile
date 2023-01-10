pipeline {
 agent none
  stages {
    stage ('Docker Build') {
      agent any
      steps {
        sh 'docker build -t dvsba:latest .'
        sh 'docker run -p 8082:8080 dvsba:latest'
      }
    }
  }
}
