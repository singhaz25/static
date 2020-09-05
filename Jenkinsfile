pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 sh 'echo "Hello World AP"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
             }
         }
         
         stage('Upload to AWS') {
              steps {
                  withAWS(credentials:'udacity') {
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacityproj3')
                  }
              }
         }
     }
}