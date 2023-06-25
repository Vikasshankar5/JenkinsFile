pipeline{
	agent any
	environment{
		name = 'Vikas'
	}
	stages{
		stage('Environment Variable'){
			steps{
				sh 'echo "${HOME}"'
				sh 'ls'
			}
		}
		stage('Variable for whole pipeline'){
			steps{
				sh 'echo "${name}"'
			}
		}
		stage('Variable for this particular stage'){
		environment{
			username = 'Alphapro'
		}
			steps{
				sh 'echo "${name}"'
				sh 'echo "${username}"'
			}
		}
		stage('Checking variable working nature for both Pipeline and particular stage'){
			steps{
				sh 'echo "${name}"'
				sh 'echo "${username}"'
			}
		}
		stage('Continue?'){
		    input{
		        message "Should we continue?"
		        ok "Yes we should!!"
		    }
		    steps{
		        sh 'echo deploy the code'
			}
		}
	}
	post{
	    always{
	        echo "Execute, no matter what!!"
	    }
	    failure{
	        echo "If failed"
	    }
	    success{
	        echo "success message"
	    }
	}
}
