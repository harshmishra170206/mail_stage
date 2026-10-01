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
                bat 'python -m py_compile app.py'
                echo 'Build successful: app.py compiled with no syntax errors'
            }
        }

        stage('Send Notification') {
            steps {
                echo "EMAIL WOULD BE SENT -> To: student@example.com | Subject: Build Notification: ${env.JOB_NAME} #${env.BUILD_NUMBER}"
            }
        }
    }
}
