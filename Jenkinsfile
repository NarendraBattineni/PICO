pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			sh 'mvn clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
    echo "deploy completed"
 			    }
 		 }
 	}
}


