/* Requires the Docker Pipeline plugin */
pipeline {
    agent { dockerfile true }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "starting uvicorn server dev mode..."'
                sh 'uvicorn main:app --host 0.0.0.0 --port 7860'
            }
        }
    }
}
