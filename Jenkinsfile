/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    tools {nodejs "NodeJS"}
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
    }
}
