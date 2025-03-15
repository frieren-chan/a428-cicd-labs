pipeline {
    agent {
        docker {
            image 'node:16-buster-slim'
            args '-p 3013:3013'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
