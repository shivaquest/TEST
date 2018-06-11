pipeline {
	    agent any
	    stages{
	        stage('Build'){
	            steps {
	               bat mvn clean
			bat mvn package	    
			  
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
