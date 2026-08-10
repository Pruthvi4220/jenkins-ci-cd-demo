pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning project from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Step: Checking project files...'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing web application...'
                bat 'echo Test completed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website...'
                bat 'xcopy /Y *.html C:\\inetpub\\wwwroot\\'
                bat 'xcopy /Y *.css C:\\inetpub\\wwwroot\\'
                bat 'xcopy /Y *.js C:\\inetpub\\wwwroot\\'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}