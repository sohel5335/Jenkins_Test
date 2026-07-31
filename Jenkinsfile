pipeline {
    agent any

    environment {
        APP_NAME = "MyWebApp"
        ENVIRONMENT = "Development"
        VERSION = "1.0.0"
    }

    stages {

        stage('Welcome') {
            steps {
                echo "Welcome to Jenkins Pipeline"
            }
        }

        stage('Application Info') {
            steps {
                echo "Application Name: ${APP_NAME}"
                echo "Environment: ${ENVIRONMENT}"
                echo "Version: ${VERSION}"
            }
        }

        stage('Finish') {
            steps {
                echo "Pipeline completed successfully."
            }
        }
    }

    post {
        always {
            echo "Pipeline execution finished."
        }

        success {
            echo "Build Status: SUCCESS"
        }

        failure {
            echo "Build Status: FAILURE"
        }
    }
}
