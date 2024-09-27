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
            // Kirim email notifikasi
            emailext (
                to: 'forestist.ipad@gmail.com',
                subject: "Build Notification: ${currentBuild.fullDisplayName}",
                body: "Build completed with status: ${currentBuild.currentResult}"
            )
        }
    }
}

