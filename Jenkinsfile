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
                 git branch: 'master', url: 'https://github.com/jitendrapsingh/pipeline1jenkinsfile'
                
            }
        }
	}
}
}
