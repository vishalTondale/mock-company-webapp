
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build the application
                    sh './gradlew assemble'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run the tests
                    sh './gradlew test'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and Tests Passed!'
        }
        failure {
            echo 'Build or Tests Failed.'
        }
    }
}
