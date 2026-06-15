pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
	
		stage('Checkout'){
			steps{
				git branch:'main',url:'https://github.com/chinmayiii/mygradlee.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle build'
			}
		}
		stage('Run'){
			steps{
				sh 'gadle run'
			}
		}
		stage('Run Applicaton'){
			steps{
				sh 'gradle display'
			}
		}
	}
	
	post{
		success{
			echo 'successfull'
		}
		failure{
			echo 'failed'
		}
	}
}
