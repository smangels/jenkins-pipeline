pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building...'
			}
		}
		stage('Test') {
			steps {
				echo 'Testing...'
				sh 'mkdir -p out/'
				sh 'touch out/file2.txt'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deploy Project...'
				sh 'tar czf Archive.tar.gz out/'
			}
		}
	}
}