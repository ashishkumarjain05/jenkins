properties([  parameters([
  credentials (credentialType: 'com.cloudbees.jenkins.plugins.awscredentials.AWSCredentialsImpl', defaultValue: '', description: '', name: 'CREDENTIALS', required: false),
  string (defaultValue: '', description: '', name: 'BucketName', trim: false),
  string (defaultValue: '', description: '', name: 'Region', trim: false),
    ])
])
  
pipeline {
    agent any
    stages {
	    stages {
        stage('git checkout') {
            steps {
                git branch: 'master', credentialsId: 'ashishcred', url: 'https://github.com/ashishkumarjain05/jenkins.git'
                
            }
        }
        stage('S3 List') {
            steps {
                sh '''
                aws s3 ls
				aws ec2 describe-instances --region ap-south-1 |grep InstanceId
				echo""
				aws s3api create-bucket --bucket my-$BucketName --region $Region'''
                
            }
        }
	}
}
