pipeline {
	    agent any
	    stages{
	        stage('Build'){
	            steps {
	                 mvn clean 
			  mvn package
	            }
	            post {
	                success {
	                    echo 'Now Archiving...'
	                    archiveArtifacts artifacts: '**/target/*.war'
	                }
	            }
	        }
	    }
	}
