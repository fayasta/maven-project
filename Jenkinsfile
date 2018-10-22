pipeline {
	  agent any
	 
	  stages {
		//Run the maven build
		stage('Build') {
		   steps {
			sh 'mvn test'
			echo 'Testing Stage...'
		  }
		}
		stage('Test') {
		  steps {
			echo 'Testing Stage...'
		  }
		}
		stage('Deploy') {
		  steps {
			echo 'Deploying Stage...'
		  }
		}
	  }
}	
