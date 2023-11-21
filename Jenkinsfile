pipeline {
    agent any
    tools {
        maven 'MavenInstallationName'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your repository
                git 'https://github.com/annemshivaji/lab32.git'
            }
        }
        
        stage('Build') {
            steps {
                // Assuming your project uses Maven, perform a Maven build
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Execute tests (if applicable)
                sh 'mvn test'
            }
        }
   
        // Add more stages as needed (e.g., additional build steps, integration, deployment, etc.)
    }
}
