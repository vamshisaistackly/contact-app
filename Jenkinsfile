pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning code'
            }
        }

        stage('Install Backend Dependencies') {
            steps {
                dir('backend') {
                    sh 'npm install'
                }
            }
        }

        stage('Start Application') {
            steps {
                dir('backend') {
                    sh 'pm2 start server.js || pm2 restart server'
                }
            }
        }
    }
}
