pipeline {
  agent { label 'vm' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    
    stage('Scan') {
      steps {
        sh 'trivy --no-progress --exit-code 1 --severity HIGH,CRITICAL darinpope/java-web-app:latest'
      }
    }
  }
}
