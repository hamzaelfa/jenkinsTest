pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/hamzaelfa/jenkinsTest.git'
            }
        }
        stage('Build and run') {
            steps {
                sh "python3 jenkinsTest.py"
            }
        }
    }
}