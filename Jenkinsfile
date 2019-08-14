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
        mail bcc: '', 
             body: '''Hi, The pipeline job for Mulesoft is completed and the project was deployed to standalone server.
                  Regards,
                  Jenkins''', 
              cc: '', 
              from: 'Jenkins@prolifics.com', 
              replyTo: '', 
              subject: 'Jenkins job for mulesoft demo', 
              to: 'narendra.battineni@prolifics.com'
    }
}
}


