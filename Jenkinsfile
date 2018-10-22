pipeline {
	  agent any
	 
	  stages {
		//Run the maven build
		stage('Build') {
			sh 'mvn test'
			echo 'Building Stage...'
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
