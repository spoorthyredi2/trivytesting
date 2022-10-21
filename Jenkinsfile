pipeline {
  agent { label 'vm' }
  
  stages {
    
    stage('Scan') {
      steps {
        sh 'trivy --no-progress --exit-code 1 --severity HIGH,CRITICAL gcr.io/leap-metrics-dev/leap-billing-service@sha256:238996df3d2491ada108ee156659bfa261506424752d8751695d2343c803a983'
      }
    }
  }
}
