pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
 			bat 'cd PICO & mvn clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
    echo "deploy completed"
 			    }
 		 }
 	}
}


