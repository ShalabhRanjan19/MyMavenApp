pipeline {
    agent any

    tools {
        jdk 'jdk-17'        // The name you set in Global Tool Configuration
        maven 'maven-3.9.0' // The name you set for Maven
    }

    stage('Checkout') {
    steps {
        git branch: 'main', 
            url: 'https://github.com/ShalabhRanjan19/MyMavenApp.git'
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

