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
            emailext(
                to: 'forestist.ipad@gmail.com',
                subject: "Build ${currentBuild.fullDisplayName} - ${currentBuild.currentResult}",
                body: "Job ${env.JOB_NAME} Build ${env.BUILD_NUMBER}\nStatus: ${currentBuild.currentResult}\nMore details: ${env.BUILD_URL}",
                attachLog: true
            )
        }
    }
}
