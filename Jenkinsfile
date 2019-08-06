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
 				sh 'mvn -f pico/pom.xml package deploy  -Dusername=mule_srivis12 -Dpassword=Mule123 -Denvironment=Sandbox -DmuleDeploy'
 			}
 		}
 	}
 }

}