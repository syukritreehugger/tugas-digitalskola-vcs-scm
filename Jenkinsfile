pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Perintah build (misalnya dengan Maven, Gradle, atau Docker)
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Perintah test (misalnya untuk unit test)
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Perintah deploy
            }
        }
    }

    post {
        always {
            echo 'Build finished'
                emailext(
                    subject: "${JOB_NAME}.${BUILD_NUMBER} PASSED",
                    mimeType: 'text/html',
                    to: "$email",
                    body: "${JOB_NAME}.${BUILD_NUMBER} PASSED"
                )
    }
}

