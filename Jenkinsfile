pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code from the repository...'
                checkout scm
            }
        }
               stage('Build') {
            steps {
                script {
                    try {
                        // Set up environment variables
                        env.PATH = "${env.JAVA_HOME}/bin:${env.MAVEN_HOME}/bin:${env.PATH}"
                        
                        // Maven build with clean and install phases
                        sh 'mvn clean install'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        echo "Build failed: ${e.message}"
                    }
                }
            }
        }

        stage('Echo Stage 1') {
            steps {
                echo 'This is Stage 1'
                echo 'Performing some actions in Stage 1...'
            }
        }
        stage('Echo Stage 2') {
            steps {
                echo 'This is Stage 2'
                echo 'Performing some actions in Stage 2...'
            }
        }
    }
}
