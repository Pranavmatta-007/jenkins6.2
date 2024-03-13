pipeline {
    agent any
    
    stages {
        stage('Stage 1') {
            steps {
                echo "Hello from Stage 1!"
            }
        }
        
        stage('Stage 2') {
            steps {
                echo "Hello from Stage 2!"
            }
        }
        
        stage('Stage 3') {
            steps {
                echo "Hello from Stage 3!"
            }
        }
    }
    
    post {
        success {
            emailext body: "Pipeline successful. See attached logs for details.",
                    subject: "Pipeline Success",
                    to: "pranav4874.be@chitkara.edu.in",
                    attachLog: true
        }
        failure {
            emailext body: "Pipeline failed. See attached logs for details.",
                    subject: "Pipeline Failure",
                    to: "pranav4874.be@chitkara.edu.in",
                    attachLog: true
        }
    }
}