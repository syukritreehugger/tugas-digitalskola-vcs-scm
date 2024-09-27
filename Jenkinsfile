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
            emailext to: 'forestist.ipad@gmail.com',
                 subject: "Job '${env.JOB_NAME}' (${env.BUILD_NUMBER})",
                 body: "Build ${currentBuild.fullDisplayName} finished with status: ${currentBuild.currentResult}",
                 attachLog: true
        }
    }
}

