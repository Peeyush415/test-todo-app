pipeline {
	agent any

	tools{
		nodejs 'NodeJS 22'
	}

	stages{
		stage('Clone Repository') {
			steps {
				git 'https://github.com/Peeyush415/test-todo-app.git'
			}
		}
		stage('Install Dependency') {
			steps{
				sh 'npm install'
			}
		}
		stage('Build') {
			steps{
				sh 'npm run start'
			}
		}
		stage('Test') {
			steps{
				echo "some test perform"
			}
		}
	}

	post {
		success {
			echo "Build Successfull"
		}
		failure {
			echo "Build Fauliure"
		}
	}
}
