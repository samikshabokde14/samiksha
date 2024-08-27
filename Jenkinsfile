pipeline{
         agent any
        triggers {
     pollSCM '* * * * *'
  }

       stages{
           stage( checkout ){
             steps{
                 git 'https://github.com/samikshabokde14/samiksha.git'
                }
             }
           stage( build ){
              steps{
                   sh 'mvn install'
                 }
                }
           stage( deployment ){
              steps{
                   sh 'cp target/samiksha.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'
                }
              }
           }
         }

