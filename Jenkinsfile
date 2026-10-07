pipeline {
    // Execute this pipeline on any available Jenkins agent
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Automatically checks out the code from the linked GitHub repository
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Replace with actual build commands, e.g.:
                // sh 'npm install' or sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Replace with actual test commands, e.g.:
                // sh 'npm test' or sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying to staging environment...'
                // Add deployment scripts here
            }
        }
    }
    
    // The post section runs after the stages complete, depending on the outcome
    post {
        always {
            echo 'Pipeline execution is complete. Cleaning up workspace...'
            cleanWs() // Optional: Cleans the workspace after the build
        }
        success {
            echo '✅ Pipeline succeeded!'
        }
        failure {
            echo '❌ Pipeline failed. Please check the Jenkins console output for details.'
        }
    }
}
