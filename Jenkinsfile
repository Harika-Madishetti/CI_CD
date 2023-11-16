pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Your npm and Node.js commands here                 
                    sh 'npm run build'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'npm test'
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    sh 'npm start'
                }
            }
        }
    }
}