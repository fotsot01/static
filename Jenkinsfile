pipeline {
      agent any 
      stages {
            stage('Lint HTML') {
                  steps {
                        sh 'echo "Linting the html code"'
                        sh 'tidy -q -e *.html'
                  }
            }
                  
          stage('Upload TO AWS NOW') {
              steps {
                   sh 'echo "Hello World"'
                   sh '''
                   echo "Multineline shell steps works too"
                   ls -lah


                   '''
                           withAWS(region:'us-east-1',credentials:'aws-static') {
                           sh 'echo "Uploading content"'
                           s3Upload(file:'index.html', bucket:'jenkins2020', path:'index.html')
                          }

              
                            
                            
                           
                       
                       
                   
                   }
                }
            }
          }
