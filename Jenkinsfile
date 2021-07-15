
pipeline
{
	stages
	{
stage('checkout')
{
  steps
{
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/KalashPalwanda/UiPath_Jenkins_CICDDemo.git']]])

   }

}


stage('Deploy to UAT') {
	            steps {
	               UiPathTest credentials: Token(accountName: 'testiqngktgo', credentialsId: 'APIUserKey'), folderName: 'Shared', orchestratorAddress: 'https://cloud.uipath.com/testiqngktgo/DefaultTenant/orchestrator_', orchestratorTenant: 'DefaultTenant', testResultsOutputPath: '', testTarget: TestProject(environments: '', testProjectPath: 'project.json')
	

		    }
	            }
	        }
}
