pipeline {
	  agent any
	 
	  stages {
		//Run the maven build
		stage('Build') {
		   steps {
			checkout scm
			echo 'Testing Stage...'
			   // -- Compilando
			   echo 'Compilando aplicación'
			   sh 'mvn clean compile'
		  }
		}
		stage('Test') {
		  steps {
			echo 'Testing Stage...'
		        echo 'Ejecutando tests'
			sh 'mvn verify'
		  }
		}
		stage('Deploy') {
		  steps {
			echo 'Deploying Stage...'
		  }
		}
	  }
}	
