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
 post {
    always {
        mail bcc: '', body: '''Hi,

this is for test.''', cc: '', from: '', replyTo: '', subject: 'Jenkins job for mulesoft demo', to: 'narendra.battineni@prolifics.com'
    }
}
}


