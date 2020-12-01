pipeline {
	agent any
	stages {
		stage('Checkout SCM') {
			steps {
				git branch: 'test', credentialsId: 'b2f1fcd4-6c85-4de0-be24-65b88d196146', url: 'https://github.com/yongyongjiejie/simple-java-maven-app'
			}
		}
	}	
	post {
		success {
			dependencyCheckPublisher pattern: 'dependency-check-report.xml'
		}
	}
}
