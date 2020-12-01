pipeline {
	agent any
	stages {
		stage('Checkout SCM') {
			steps {
				git branch: 'master', credentialsId: 'aa7ce681-cf84-4bb1-a1a6-a7012789b2ba', url: 'https://github.com/yongyongjiejie/simple-java-maven-app.git'
			}
		}
	}	
	post {
		success {
			dependencyCheckPublisher pattern: 'dependency-check-report.xml'
		}
	}
}
