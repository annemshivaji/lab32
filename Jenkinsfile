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
                echo 'This is Stage 1'
                echo 'Performing some actions in Stage 1...'
            }
        }
   
    }
}
