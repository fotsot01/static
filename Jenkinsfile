pipeline {
      agent any 
      stages {
          stage('Upload TO AWS') {
              steps   {
                   sh 'echo "Hello World"'
                   sh '''
                   echo "Multineline shell steps works too"
                   ls -lah
                     withAWS(region:'us-east-1',credentials:'aws-static') {
                           sh 'echo "Uploading content"'
                            s3Upload(file:'index.html', bucket:"Jenkins2020")
                            '''
                       }
                       
                   
                   }
                  }
                 }
                }
