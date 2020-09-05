pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
              steps {
                    s3Upload(acl: 'PublicReadWrite', bucket: 'udacityproj3', file: 'index.html', pathStyleAccessEnabled: true, payloadSigningEnabled: true)
              }
         }
     }
}