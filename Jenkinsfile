pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 tools {
       maven 'maven'
       jdk 'jdk'
 }
 stages {
 	stage ('Build'){
 		steps {
 			     bat 'mvn clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
    echo "deploy completed"
 			    }
 		 }
 	}
}


