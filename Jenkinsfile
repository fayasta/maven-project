pipeline {
	  agent any
	 
	  stages {
		//Run the maven build
		stage('Build') {
		   steps {
			echo 'Testing Stage...'
			sh 'mvn clean package'
		  }
		}
		  post{
			  success{
			  echo 'Now archiving...'
				  archiveArtifacts artifacts: '**/target/*.war'
			  }
		  }
	  }
}	
