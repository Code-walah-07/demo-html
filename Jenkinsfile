pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/Code-walah-07/demo-html.git'
            }
        }

        stage('Setup Python Environment') {
            steps {
                bat 'python -m venv venv'
                bat '.\\venv\\Scripts\\activate && pip install -r requirements.txt'
            }
        }

        stage('Run Python Script') {
            steps {
                bat '.\\venv\\Scripts\\activate && python demo-file.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat '.\\venv\\Scripts\\activate && pytest tests/'
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded!'
        }
        failure {
            echo '❌ Build failed. Check logs.'
        }
    }
}

