pipeline {
    agent any

    
    stages {
        stage('CFDeploy') {
            steps {
                sh "aws cloudformation create-stack --stack-name cfn-demo --template-body file://02a_basic-vpc.yml"
            }
        }
    }
}
