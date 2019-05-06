node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat 'dotnet build Test.sln'

	stage 'Publish'
		bat 'rmdir D:\Jenkins\workspace\Test\Test\app /s /q'
		bat 'dotnet publish Test.sln -c release -o app/'

}
