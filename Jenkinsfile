pipeline {
<<<<<<< HEAD
  agent any 
  stages {
    stage(‘Build’) {
      steps {
        sh ‘echo “Hello World”’
        sh ‘“
                  echo “Multiline shell steps works too”
                  ls -lah
               “‘
      }
    }
  }
}
=======
     agent any
     stages {
         stage('Build') {
             steps {
                 sh 'echo "Hello World"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
             }
         }
         stage('Lint HTML') {
              steps {
                  sh 'tidy -q -e *.html'
              }
         }
         
	 stage('Upload to AWS') {
             steps {
                 sh 'echo "Hello AWS"'
                 sh '''
                     echo "Here is multiline shell steps"
                     ls -lah
                 '''
                  withAWS(region:'eu-west-1',credentials:'aws-static') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'static-jenkins-pipeline')
                  }
              }
         }
     }
}
>>>>>>> 6847397e422bf4cdf1a79bd905a6621809bf1659
