pipeline {
    agent any

    tools {
        // Configure the JDK version
        jdk 'JDK 17' // This name should match the name you entered in the Global Tool Configuration
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

