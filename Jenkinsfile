pipeline {
    agent any

    parameters {
        choice(
            name: 'EnvironmentName',
            choices: ['dev', 'qa', 'test', 'prod'],
            description: 'Choose the environment to use for this pipeline.'
        )
    }

    stages {
        stage('Build') {
            steps {
                echo '🔧 Building...'
                echo "Running Build ID: ${env.BUILD_ID}"
                echo "Jenkins URL: ${env.JENKINS_URL}"
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Testing...'
                echo "Selected Environment: ${params.EnvironmentName}"
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying...'
                echo "Deploying to ${params.EnvironmentName} environment"
            }
        }
    }
}

