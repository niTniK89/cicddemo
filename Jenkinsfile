pipeline
{
	agent any
	stages{
		stage('Build Application'){
		steps{
		bat 'mvn package -DskipTests'
		}
		}
		
		stage('MUnit Test Application'){
		steps{
		bat 'mvn test'
		}
		}
		
		stage('Deploy Application to CloudHub'){
		steps{
		bat 'mvn package deploy -DmuleDeploy'
		}
		}
		
		stage('Perform Regression Testing'){
		steps{
		bat 'C:\\Users\\NitishJain\\AppData\\Roaming\\npm\\newman run C:\\nik\\newman\\test_coll12may.postman_collection.json -r htmlextra --reporter-htmlextra-export C:\\nik\\newman'
		}
		}
}
}