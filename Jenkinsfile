node {
	stage ('Clean'){
		bat'rd -f Test' 
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
}
