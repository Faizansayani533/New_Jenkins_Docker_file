# Jenkins
pipeline 
{
    agent any
    environment {
	DOCKER_IMAGE = 'hello-world-python:1.0'
}	
    stages {
        stage('Checkout') {
            steps {
	       git branch:'main', url:https://github.com/Faizansayani533/New_Jenkins_Docker_file.git
	}
      }		
    stage('Docker Build') {
	steps {
	  if (fileExists('Dockerfile')) {
		sh "docker build -t $(env.DOCKER_IMAGE)
		} else {
		  error"Dockerfile not found int the workspace."
		}	]
    stage('Docker Run (Optional)'){
	steps {
	  sh "docker run -rm $(env.DOCKER_IMAGE)"
	}	} }
    post {
	success {  echo 'python application Docker image built successfully'  }
	failure{
	   echo 'Docker build or run failed'
	} } }
            
