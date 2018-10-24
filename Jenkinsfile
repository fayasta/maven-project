pipeline {
	  agent any
	 
	  stages {
		//Run the maven build
		stage('Build') {
		   steps {
			echo 'Testing Stage...'
			//sh 'mvn clean package'
		  }
		  post{
			  success{
			  	echo 'Now archiving...'
			//	archiveArtifacts artifacts: '**/target/*.war'
			  }
		  }
		}
		  stage('Deploy to Dev'){
			  steps{
			  //	build job: 'Deploy-To-Dev'
				  echo 'Code deployed to DEV'
			  }
		  }
		  stage('Deploy to Prod'){
			  steps{
				  timeout(time:5, unit:'DAYS'){
				  	// input message:'Approve PRODUCTION Deployment?'
				  }				 
				//  build job: 'Deploy-To-Prod'
			  }
			  post{
				  success{
				  	echo 'Code deployed to Production'
				  }
				  
				  failure{
					echo 'Deployment failed'
				  }
			  }
		  }
	  }
}	
