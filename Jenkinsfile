/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
      docker {
        image 'node:latest'
        args '--volume /var/run/docker.sock:/var/run/docker.sock'
      } 
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run test'
            }
        }
    }
}
