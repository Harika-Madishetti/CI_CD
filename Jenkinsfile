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
                    sh './scripts/test.sh'
                }
            }
        }
    }
    post {
        always {
            echo 'Test! Sending email notification...'
            emailext subject: 'Build Failed: ${currentBuild.fullDisplayName}',
                      body: 'The build has failed. Please investigate the issue.',
                      to: 'harikamadishetti12@gmail.com', 
                      attachLog: true
        }
    }
}