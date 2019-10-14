pipeline {
	agent any

	stages
	{
		stage('Build Image')
		{
			steps
			{
				script {
					bat 'docker build . -t blagged:1.0'
				}
			}
		}
	}
}
