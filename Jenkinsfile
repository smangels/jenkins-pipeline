pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building...'
				sh 'sleep 3'
				sh 'mkdir -p out/'
				sh 'echo $(date +"%T") > out/file2.txt'
			}
		}
		stage('Test') {
			steps {
				echo 'Testing...'
				archiveArtifacts artifacts: '**/out/*.txt', fingerprint: true
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deploy Project...'
				cleanWs()
			}
		}
	}
}