pipeline{
    agent any
    tools{
        maven 'mymaven'
    }
    stages{
        stage('Checkout  code'){
	        steps{
		        echo 'cloning the repo'
                git 'https://github.com/adhongade1/DevOpsCodeDemo.git'
            }
        }
        stage('Compile'){
            steps{
                  echo 'complie the code again..'
                  sh 'mvn compile'
            }
        }
        stage('CodeReview'){
            steps{
        		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
            }
        }
        stage('UnitTest'){
		    steps{
	               sh 'mvn test'
            }
        }
        stage('Package'){
		    steps{
		            sh 'mvn package'
            }
        }
	}
}
