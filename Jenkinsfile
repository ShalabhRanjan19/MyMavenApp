pipeline {
    agent any

    tools {
        jdk 'jdk-17'        // The name you set in Global Tool Configuration
        maven 'maven-3.9.0' // The name you set for Maven
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/your-repo-name.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}

