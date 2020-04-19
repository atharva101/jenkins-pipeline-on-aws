pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'aws-static') {
          s3Upload(bucket: "jenkins-bucket-udacity", file:'index.html')
        }
      }
    }
  }
}