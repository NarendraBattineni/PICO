pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			withMaven(maven:'maven'){
 				sh 'mvn -f pico/pom.xml clean install'
 			}
 		}
 	}
 	stage ('Deploy'){
 		steps {
 			withMaven(maven:'maven'){
 				sh 'mvn -f pico/pom.xml package deploy  -Dusername=$ANYPOINT_USR -Dpassword=$ANYPOINT_PSW -Denvironment=Development -DmuleDeploy'
 			}
 		}
 	}
 }

}
