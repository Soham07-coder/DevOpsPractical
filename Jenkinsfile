// Jenkinsfile

pipeline {
    // 1. Agent: Defines where the pipeline runs (using any available Jenkins agent/node)
    agent any

    // 2. Stages: The core of the CI/CD process
    stages {
        
        // --- STAGE 1: Build ---
        stage('Build') {
            steps {
                echo 'Starting the Build stage...'
                // REPLACE THIS with your actual build command (e.g., mvn clean install)
                sh 'echo "Running compilation/packaging command..."' 
                echo 'Build complete.'
            }
        }
        
        // --- STAGE 2: Test ---
        stage('Test') {
            steps {
                echo 'Starting the Test stage...'
                // REPLACE THIS with your actual test command (e.g., mvn test)
                sh 'echo "Running unit and integration tests..."'
                // NOTE: A failing command here will stop the pipeline
                echo 'Tests passed.'
            }
        }
        
        // --- STAGE 3: Deploy ---
        stage('Deploy') {
            steps {
                echo 'Starting the Deploy stage...'
                // REPLACE THIS with your actual deployment command (e.g., scp, docker push, server restart)
                sh 'echo "Deploying built artifact to target environment..."'
                echo 'Deployment finished successfully.'
            }
        }
    }
    
    // 3. Post-Actions: Runs after all stages are done
    post {
        always {
            echo 'Pipeline execution complete. See logs for details.'
        }
        success {
            echo 'CI/CD Pipeline ran successfully! 🎉'
        }
    }
}
