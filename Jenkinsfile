pipeline {
	agent any 
	parameters {
  choice choices: ['DEV', 'UAT', 'QA', 'PROD'], description: 'parameterized', name: 'Environment'
}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			   sh '/home/shantanu/Downloads/apache-tomcat-9.0.82/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh cp  'cp target/CICD.war /home/shantanu/Downloads/apache-tomcat-9.0.82/webapps'
			}}	
}}
