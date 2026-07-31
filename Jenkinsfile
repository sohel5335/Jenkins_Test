pipeline {
    agent any

    parameters {
        choice(
            name: 'ENV',
            choices: ['DEV', 'QA', 'PROD'],
            description: 'Select Environment'
        )
    }

    stages {
        stage('Check Environment') {
            steps {
                script {
                    echo "Selected Value: '${params.ENV}'"

                    if (params.ENV == "DEV") {
                        echo "Development Environment Selected"
                    } else if (params.ENV == "QA") {
                        echo "QA Environment Selected"
                    } else {
                        echo "Production Environment Selected"
                    }
                }
            }
        }
    }
}
