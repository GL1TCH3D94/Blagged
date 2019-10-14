node{
def blagged
stage('Clone Repository')
{
	checkout smc
}
stage('Build')
{steps
	{
		blagged = docker.build("jhop94/blagged")
	} 
}
stage('Push image')
{
	docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials')
	{
		app.push("${env.BUILD_NUMBER}")
		app.push("latest")
	}
}
}
