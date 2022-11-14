pipeline {
    agent any
    stages { 
        stage('checkout') {
		   steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Ssases/cloudform.git']]])
           }
        }
        stage('cfn stack deploy for testing for test') {
            steps {
            sh ' aws cloudformation deploy --template-file ec2.yaml --stack-name ec2-creation'
            }
        }
    }
}
		   
