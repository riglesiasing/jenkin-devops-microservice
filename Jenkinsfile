
pipeline {
     //agent {
       // docker { image 'maven:3.6.3' }
    //}
    agent any
	
    environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
  }
	
   stages {
       stage('Build') {
           steps {   
               sh 'mvn --version'		   
			   echo "Build"  	
           }
       }
       stage('Test') {
           steps {
             echo "Test" 
           }
       }
	   stage('Integration Test') {
           steps {
             echo "Integration Test" 
           }
       }
   }
}
