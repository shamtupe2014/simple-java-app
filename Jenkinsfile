pipeline {
    agent any

    tools {
        maven 'Maven' // Name configured in Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shamtupe2014/simple-java-app.git'
            }
        }
        
        stage('Build') {
            steps {
                // Use Maven tool configured in Jenkins
                withMaven(maven: 'Maven') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Test') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}

