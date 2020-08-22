pipeline{
  agent any
  tools { 
       maven 'Maven3.6.3'
	}
  stages {
       stages('SCM Checkout') {
 	  steps {
 		 git 'http://github.com/Herafatimaalvi/TestApp'
		}
	  }
	stage('Compile-package') {
	   steps {
		sh "mvn -version"
		sh "mvn clean install"
		sh "mvn package"
		}
	     }
  }
   post {
      always {
	cleanWS()
	}
       }
}
