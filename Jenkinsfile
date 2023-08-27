/* Requires the Docker Pipeline plugin */
pipeline {
    agent { dockerfile true }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
                sh 'svn --version'
                sh 'python --version'
                sh 'echo "starting uvicorn server dev mode..."'
                sh 'pip install uvicorn'
                sh 'uvicorn main:app --reload'
            }
        }
    }
}
