pipeline{
	agent any	

	stages{
		stage("TEST"){
			
			steps{
				echo "Testing for $BRANCH_NAME"
			}
		}
		stage("BUILD"){
			when{
				expression{
				 BRANCH_NAME=='DEV' || BRANCH_NAME=='PROD'
				}
			}
			steps{
				echo "Building for $BRANCH_NAME"
			}
		}
		stage("DEPLOY"){
			when{
				expression{
				 BRANCH_NAME=='PROD' || BRANCH_NAME=='master'
				}
			}
			steps{
				echo "Deploying for $BRANCH_NAME"
			}
		}

	}
}