pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/hamzaelfa/jenkinsTest.git']]])
            }
        }
        stage('Build and run') {
            steps {
                sh "python3 ./src/mymodule.py"
            }
        }
        stage('Test') {
            steps {
                sh 'echo $PATH'
                sh 'which pytest'
                sh 'pytest tests'
            }
        }

    }
}