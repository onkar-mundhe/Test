pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                checkout scm
            }
        }
        
        stage('Environment Info') {
            steps {
                echo 'Displaying environment information...'
                sh 'echo "Current directory: $(pwd)"'
                sh 'echo "Files in directory:"'
                sh 'ls -la'
                sh 'echo "Node version:"'
                sh 'node --version || echo "Node not found"'
                sh 'echo "NPM version:"'
                sh 'npm --version || echo "NPM not found"'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Build stage - This is where your build commands would go'
                sh 'echo "Build completed successfully!"'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test stage - This is where your tests would run'
                sh 'echo "Tests completed successfully!"'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully! 🎉'
        }
        failure {
            echo 'Pipeline failed! ❌'
        }
        always {
            echo 'Pipeline finished.'
        }
    }
}