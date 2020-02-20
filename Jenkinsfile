pipeline {
      agent any 
      stages {
          stage('Upload TO AWS') {
              steps {
                   sh 'echo "Hello World"'
                   sh '''
                   echo "Multineline shell steps works too"
                   ls -lah
                     withAWS(region:'us-east-1',credentials:'Jenkins') 
                          
                            { s3Upload(file:'index.html', bucket:'Jenkins2020', path:'index.html)
                            
                            
                           
                       }
                       
                   
                   }
                  }
                 }
                }

