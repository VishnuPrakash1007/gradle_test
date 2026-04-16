pipeline {
    agent any  

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/VishnuPrakash1007/gradle_test.git'
            }
        }

        stage('Setup') {
            steps {
                sh 'chmod +x gradlew'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        
        stage('Run Application') {
            steps {
                sh './gradlew run'
            }
        }
    }

    post {
        success {
            echo 'Build and execution successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
