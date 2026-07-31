pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['Development', 'Testing', 'Production'],
            description: 'Select the deployment environment'
        )
    }

    stages {
        stage('Show Environment') {
            steps {
                echo "Selected Environment: ${params.ENVIRONMENT}"
            }
        }
    }
}
