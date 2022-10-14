pipeline {
    agent {
        docker {
            image 'node:18-alpine' 
            args '-p 4000:4000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
    stage('Test') {
        steps {
                sh './jenkins/scripts/test.sh'
            }
        }
}