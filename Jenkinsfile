pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo Build stage'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Test stage'
            }
        }
         stage('Deliver for development') {
            when {
                branch 'development'
            }
            steps {
                sh 'echo dev branch'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh 'echo dev done'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                sh 'echo prod branch'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh 'echo prod done'
            }
        }
    }
}
