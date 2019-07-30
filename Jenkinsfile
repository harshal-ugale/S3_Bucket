pipeline{
	agent any
	stages{
	stage('Clone Repo') {
		steps {
			sh "export AWS_DEFAULT_REGION=us-east-1"
			sh "aws cloudformation create-stack --stack-name ${params.Stackname} --template-body file://test 2 CFT FOR S3.json --region 'us-east-1' --parameters ParameterKey='BucketName',ParameterValue=${params.Bucketname}" 
			}
	  }
	}
}
