pipeline {
	agent any
	//agent {
	//	docker { image 'node:latest'}
	//}
	stages {
		stage ("Build") {
			steps {
				sh 'hostname -f'
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
