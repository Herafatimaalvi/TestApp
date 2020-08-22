pipeline {
 agent any
tools {
   maven 'Maven3.6.3'
}
 stages {
   stage('SCM CheckOut'){
      steps {
        git 'https://github.com/Herafatimaalvi/TestApp'
        }
        }
        stage('Compile-Package'){
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
     
