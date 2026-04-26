pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'docker build -t pipeline-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases...'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker run -d -p 5000:5000 pipeline-app'
            }
        }
    }
}