pipeline {

    agent any

    stages {
        stage('CFDeploy') {
            steps {
                withAWS(credentials: 'frescolab', region: 'us-east-1')
                sh "aws cloudformation create-stack --stack-name cfn-demo --template-body file://02a_basic-vpc.yml --region 'us-east-1'"
            }
        }
    }
}