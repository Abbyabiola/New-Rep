pipeline{
	agent any
	stages{
		stage('1-clonecode'){
			steps{
				sh 'ped'
			}
		}
		stage('2-artifactbuild'){
			steps{
				sh 'systemctl status jenkins'
			}
		}
		
            
		stage('4-unitest'){
			steps{
				echo "we are in stage 3"
			}
		}
	}
    stage('4-deploy'){
        steps{
            sh 'lsblk'
        }
    }

}
