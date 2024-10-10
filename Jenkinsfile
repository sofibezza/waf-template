#!groovy
@Library('shared-library-devops')_

pipeline {
    agent {
        kubernetes {
            label 'cloudformation-deployer'
            defaultContainer 'cf-deployer'
        }
    }
    stages {
        stage('cloudformation-deployer') {
            steps {
                cloudFormationDeployer iacPath: "iac", params: "--ask"
            }
        }
    }
}
