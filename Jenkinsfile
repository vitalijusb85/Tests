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
			
		bat 'cd Test && docker run -it -p 5000:80 test'
	}
	
}
