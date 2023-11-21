pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code from the repository...'
                checkout scm
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
