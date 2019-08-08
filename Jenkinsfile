pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			sh 'mvn -p clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
    sh 'mvn deploy -p cloudHubDeployment -Dusername=${ANYPOINT_USR} -Dpassword=${ANYPOINT_PSW} -Denvironment=Sandbox -DmuleDeploy'
 			    }
 		 }
 	}
}


