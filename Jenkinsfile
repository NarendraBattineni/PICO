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
        bat 'move *.jar D:/Srivis-Mule-Training/mule-enterprise-standalone-4.2.1/apps'
 			    }
 		 }
 	}
}


