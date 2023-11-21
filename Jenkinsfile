pipeline {
    agent any

    environment {
        MAVEN_HOME = 'C:\\path\\to\\maven'
        JAVA_HOME = 'C:\\path\\to\\java'
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
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        echo "Build failed: ${e.message}"
                    }
                }
            }
        }
    }
}
