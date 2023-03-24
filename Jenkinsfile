pipeline {
    agent any

    tools {
        // Configure the Maven version
        maven 'Maven 3.8.1' // Replace with the appropriate version installed on your Jenkins instance
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
}

