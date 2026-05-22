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
        
        stage('SonarQube Analysis') {
            steps {
                 withSonarQubeEnv('sonar') {
                 sh 'mvn sonar:sonar'
         }
       }
        }

        stage('Quality Gate') {
            steps {
              waitForQualityGate abortPipeline: true
               }
          }   
        
    }
}
