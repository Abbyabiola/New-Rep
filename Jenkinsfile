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
		stage('3-unitest'){
        parallel{
            stage('unitest'){
                steps{
                    sh 'whoami'
                }
            }
            
		stage('3-unitest'){
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
}
}