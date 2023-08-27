/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.11.4-alpine3.18' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "starting uciorn server..."'
                sh 'uvicorn main:app --reload'
            }
        }
    }
}
