pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "/home/user/.git/"
        TESTING_ENVIRONMENT = "Testing Environment"
        PRODUCTION_ENVIRONMENT = "Munasinghe P M Y Gunasinghe-Production"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting  approval"
                sleep(time: 10, unit: 'SECONDS')
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
