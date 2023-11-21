pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your repository
                git 'YOUR_REPOSITORY_URL'
            }
        }
        stage('Build') {
            steps {
                // Build your Java project using Maven
                sh 'mvn clean install'
            }
        }
    }
}
