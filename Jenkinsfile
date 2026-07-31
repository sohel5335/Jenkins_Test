pipeline {
    agent any

    parameters {
        string(
            name: 'APP_NAME',
            defaultValue: 'MyWebApp',
            description: 'Enter Application Name'
        )

        booleanParam(
            name: 'DEPLOY',
            defaultValue: false,
            description: 'Deploy Application?'
        )
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${params.APP_NAME}..."
            }
        }

        stage('Deploy') {
            when {
                expression {
                    return params.DEPLOY
                }
            }

            steps {
                echo "Deploying ${params.APP_NAME}..."
            }
        }

        stage('Summary') {
            steps {
                echo "Application Name : ${params.APP_NAME}"
                echo "Deploy Selected  : ${params.DEPLOY}"
            }
        }
    }

    post {
        always {
            echo "Pipeline execution completed."
        }

        success {
            echo "Build completed successfully."
        }

        failure {
            echo "Build failed."
        }

        cleanup {
            echo "Cleaning up workspace..."
        }
    }
}
