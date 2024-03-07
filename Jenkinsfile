pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Ajitcloud/CICD.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean install' // Example build command (replace with your build command)
            }
        }
    }
    
    post {
        success {
            // Trigger success notification
            echo 'Build successful'
        }
        failure {
            // Trigger failure notification
            echo 'Build failed'
        }
    }
}

