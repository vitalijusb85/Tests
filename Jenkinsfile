node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat 'dotnet build Test.sln'

	stage 'Publish'
		bat 'dotnet publish -c releae - app/'

}
