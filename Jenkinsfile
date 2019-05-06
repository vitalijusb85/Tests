node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat' cd Test'
		bat 'dotnet build '

	stage 'Publish'
		bat ' rd -r app'
		bat 'dotnet publish -c release -o app'

}
