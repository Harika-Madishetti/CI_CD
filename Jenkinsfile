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
        stage("Test"){
            steps{
                script {
                  sh './jenkins_script/test.sh'  
                }
            }
        }
    }
    post {
        always {
            emailext (
                subject: "email",
                body: "Check the build log for details.",
                to: 'harikamadishetti12@gmail.com'
            )
        }
    }
}