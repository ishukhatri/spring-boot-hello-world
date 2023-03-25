pipeline {
    agent any

    tools {
        // Configure the Maven version
        maven 'Maven 3.8.1' // Replace with the appropriate version installed on your Jenkins instance
    }

    environment {
        // Set the build number to the current date and time
        BUILD_NUMBER = new Date().format("yyyyMMddHHmmss")
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        always {
            // Archive the built artifact with a unique name
            archiveArtifacts artifacts: 'target/*.jar', fingerprint: true, onlyIfSuccessful: true
        }
    }
}