pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
              steps {
                  withAWS(region:'us-east-1',credentials:'udacity-jenkins-user') {
                  sh 'echo "Uploading AWS"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'aws-vitor-jenkins-website')
                  }
              }
         }
     }
}