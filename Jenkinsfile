pipeline {
    agent any  

    tools {
        jdk 'JDK17'   // name must match Jenkins config
    }

    stages {
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
}
