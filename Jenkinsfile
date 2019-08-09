pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 tools {
       maven 'maven'
       jdk 'JAVA_HOME'
 }
 stages {
 	stage ('Build'){
 		steps {
 			     bat 'mvn clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
        bat 'cd target & move *.jar C:/mule-enterprise-standalone-4.2.1/apps'
 			    }
 		 }
 	}
}


