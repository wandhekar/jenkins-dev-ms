pipeline {
	agent any
	environment {
		dockerPath = tool 'MyDocker'
		mavenPath = tool 'myMaven'
		PATH ="$PATH:$dockerPath/bin:$mavenPath/bin"
	}
	
	stages {
		stage ("Build") {
			steps {
				sh 'mvn --version'
				sh 'docker version'
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
