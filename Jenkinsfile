pipeline {
	//agent any
	agent {
		docker { image 'maven:3.6.3'}
	}
	stages {
		stage ("Build") {
			steps {
				sh 'mvn --version'
				echo "build"
			}
		}
		stage ("Test") {
			steps {
				echo "Test"
			}
		}
	} 
	post {
		always {
			echo " I run always :) "
		}
		success {
			echo "I run when success"
		}
		failure {
			echo "I run on failure"
		}
	}

}
