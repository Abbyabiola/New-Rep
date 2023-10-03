pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo 'Building...'
			}
		}
		stage('Test'){
			steps{
				parallel(
					unitTests: {
						echo 'Running unit tests...'
					},
					integrationTests: {
						echo 'Running integration tests...'
					},
					systemTests: {
						echo 'Running system tests...'
					}
				)
			}
		}
		stage('Deploy'){
			steps{
				echo 'Deploying...'
			}
		}
		stage('Release'){
			steps{
				parallel(
					chrome: {
						echo 'Testing Chrome...'
					},
					firefox: {
						echo 'Testing Firefox...'
					},
					safari: {
						echo 'Testing Safari...'
					}
				)
					}
				
			}
			stage('Notify'){
				steps{
					echo 'Notifying...'
				}
			}
			stage('Securitytest'){
				steps{
					sh 'pwd'
				}
			}
		}
}
	
