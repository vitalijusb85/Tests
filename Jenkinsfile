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
			
		bat 'cd Test && docker build -t test .'
	}

	stage ('Docker Run'){
			
		bat 'winpty docker.exe run -it -p 5002:80 test'
	}
	
}
