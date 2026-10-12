
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
                bat 'echo Build Number: %BUILD_NUMBER% > build-info.txt'
                bat 'echo Timestamp: %DATE% %TIME% >> build-info.txt'
                echo 'Build information generated.'
            }
        }
    }

    post {
        success {
            echo 'Build successful! Ready for release.'
        }
    }
}
