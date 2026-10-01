pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/harshmishra170206/mail_stage.git'
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Users\\Harsh\\AppData\\Local\\Programs\\Python\\Python311\\python.exe" -m py_compile app.py'
                milestone(1)
                echo 'Build stage passed milestone 1'
            }
        }

        stage('Deploy') {
            steps {
                milestone(2)
                echo 'Deploying application...'
            }
        }
    }
}
