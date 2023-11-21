pipeline {
    agent any

    environment {
        MAVEN_HOME = 'C:\Program Files\apache-maven-3.9.5'
        JAVA_HOME = 'C:\Program Files\Java'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    try {
                        // Set up environment variables for Windows
                        bat "set PATH=%JAVA_HOME%\\bin;%MAVEN_HOME%\\bin;%PATH%"

                        // Maven build with clean and install phases
                        bat 'mvn clean install'
                    } 
                }
            }
        }
    }
}
