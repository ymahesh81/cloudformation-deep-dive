pipeline {
    agent any

    stages {
        stage('CFDeploy') {
            steps {
                script {
                    // Use the 'withAWS' step to set AWS credentials and region
                    withAWS(credentials: '62c512b5-fadd-4640-82b2-dc46bfe7884f', region: 'us-east-1') {
                    sh "aws cloudformation create-stack --stack-name cfn-demo --template-body file://02a_basic-vpc.yml --region us-east-1"
                    }
                }
            }
        }
    }
}
