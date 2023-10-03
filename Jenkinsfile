
pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo "Building the project"
			}
		}
		stage('test'){
			steps{
				sh 'systemctl start jenkins'
			}
		}
		stage('parallel'){
			parallel{
				stage('parallel-1'){
					steps{
						sh 'lscpu'
					}
				}stage('Deploy'){
					steps{
						sh 'free -m'
					}
				}
				stage('parallel-2'){
					parallel{
						stage('parallel-2-1'){
							steps{
								sh 'cat /etc/passwd'
							}
						}
					}
				}
			}
		}
	}
}
