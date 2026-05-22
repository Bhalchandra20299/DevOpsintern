pipeline {
    agent any

    tools {
        maven 'Maven-3.9.9'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
