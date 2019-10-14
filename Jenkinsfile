node{

stage('Clone Repository')
{
	checkout scm
}
stage('Build Image')
{steps
	{
		sh sudo docker build . -t blagged:1.0
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
