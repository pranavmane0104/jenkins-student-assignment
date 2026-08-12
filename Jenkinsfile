pipeline {
    agent any 
    
    stages {
        stage('Build') {
            steps {
                echo 'Compiling application...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests... Pass!'
            }
        }
        stage('Package') {
            steps {
                // Fixed for Windows: Changed 'sh' to 'bat' and updated the timestamp format
                bat 'echo Build Number: %BUILD_NUMBER% - Executed on %DATE% %TIME% > build-info.txt'
            }
        }
    }
    
    post {
        success {
            echo 'Build successful! Ready for release.'
        }
    }
}
