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
    }
}