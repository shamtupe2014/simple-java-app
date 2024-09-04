pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Clean and compile using Maven
                sh 'mvn clean compile'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests using Maven
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                // Package the application
                sh 'mvn package'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy step (for demo, we just echo)
                echo 'Deploying the application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}

