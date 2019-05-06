node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat' cd Test'
		bat 'dotnet build '

	stage 'Publish'
		bat ' if exist app\ rd -r app'
		bat 'dotnet publish -c release -o app'

}
