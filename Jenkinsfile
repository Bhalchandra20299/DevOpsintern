pipeline {
    agent any

    tools {
        maven 'Maven-3.9.9'
    }

    stages {
        
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
