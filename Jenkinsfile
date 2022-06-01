pipeline
{
	agent any
	stages{
	 stage('Build Application'){
	 steps{
	 bat 'mvn clean install'
	 }
	 }
	 
	 stage('Sonarqube Check'){
	 steps{
	 bat 'mvn sonar:sonar'
	 }
	 }
	 
	 stage('Deploy Application to Mulesoft Cloudhub'){
	 steps{
	 bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=4.4.0 -Danypoint.username=bhargaviab -Danypoint.password=Bhargavi@123 -Denv=Sandbox -Dappname=patient-demo-project -Dbusiness=Capgemini -DvCore=Micro -Dworkers=1 -DaltDeploymentRepository=myinternalrepo::default::file:///C:/snapshots'
	 }
	 }
	 
	}
}