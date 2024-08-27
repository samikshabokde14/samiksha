pipeline {
	agent any
	
	parameters {
  choice choices: ['DEV', 'QA', 'UAT'], name: 'ENVIRONMENT'
}


	stages {
	    stage('Checkout') {
	        steps {
			https://github.com/samikshabokde14/samiksha.git			       
		      }
		stage('Build') {
	           steps {
			  sh 'mvn install'

	                 }}
		stage('Deployment'){
		    steps {
			script {
			 if ( "${env.ENVIRONMENT}" == 'QA' ){
        	sh 'cp target/samiksha.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'

        	echo "deployment has been done on QA!"
			 }
			elif ( "${env.ENVIRONMENT}" == 'UAT' ){
    		sh 'cp target/samiksha.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'

    		echo "deployment has been done on UAT!"
			}
			echo "deployment has been done!"
			fi
			
			}}}	
}}
