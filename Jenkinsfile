node {
	stage ('Clean'){
		deleteDir()
	}
	stage ('Checkout'){
		checkout scm
	}
	stage ('Build'){
		bat' cd Test'
		bat 'dotnet build '
	}
	stage ('Publish'){
		bat 'dotnet publish -c release -o app/'
	}
	stage ('Docker Build'){
		
		bat 'dir'
		bat 'docker build -t test .'
	}
}
