pipeline {
    agent { docker {image 'node-alpine'}}
    stages {
        stage('Building Image') {
            steps {
                sh 'node --version'
                //sh """docker build -t first:latest."""
            }
        }
        stage('Running Container') {
            steps {
                echo "Step 2: Running Container"
                //sh """docker run -p 3030:3030 first:latest"""
            }
        }
        stage('deploy') {
            steps {
                echo "Step 3: Deploying"
            }
        }
    }
    post{
        always{
            echo 'I always Run'
        }
        success{
            echo 'I run when the job is successful'
        }
        failure{
            echo 'I run when the job fails'
        }
    }
}