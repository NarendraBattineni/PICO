pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			sh 'mvn clean test'
 		}
 	}
 	stage ('Deploy'){
 		steps {
    echo "deploy completed"
 			    }
 		 }
 	}
}


