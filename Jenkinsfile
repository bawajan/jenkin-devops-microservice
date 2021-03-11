//DECLARATIVE
pipeline {
	//agent any  // Agent here is like a node where the Build runs -Same "agent" will be referred in Azure PipeLines as well
	agent { docker { image 'maven:3.6.3'} }
	stages {
		stage ('Build') {
			steps {
				echo "Build"
				sh 'mvn --version'
			}
		}
		stage ('Test') {
			steps {
				echo "Test"
			}
		}
				stage ('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo "I run always"
		}
		success {
			echo "I run when you are successfull"
		}
		failure {
			echo "I run when you fail"
		}
	}
}