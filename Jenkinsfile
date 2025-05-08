pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Code-walah-07/demo-html.git'

            }
        }

        stage('Setup Environment') {
            steps {
                echo 'No environment setup required for HTML project.'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running HTML project...'
                // Example: if you have a build step (like copying files)
            }
        }

        stage('Run Tests') {
            steps {
                echo 'No tests defined for this HTML project.'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo ' Build failed. Check logs.'
        }
    }
}
