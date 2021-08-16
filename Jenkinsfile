pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "aws cloudformation update stack --stack-name appStack --template-body file://guestbookAS.yaml --region 'us-west-2'"
            }
        }
    }
}
