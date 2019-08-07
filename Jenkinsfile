pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			sh 'mvn -f mule-jenkins-pipeline/pom.xml clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
 			sh 'mvn -f mule-jenkins-pipeline/pom.xml package deploy  -Dusername=$ANYPOINT_USR -Dpassword=$ANYPOINT_PSW -Denvironment=Development -DmuleDeploy'
 			}
 		}
 	}
 }

}
