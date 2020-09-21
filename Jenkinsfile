
pipeline {
    agent any

    stages {
        stage('Testing') {
            steps {
                echo 'Testing Starts'
                sh 'mvn test'
                echo 'Testing Ends'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
                sh 'mvn clean package'
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploy'
                
            }
        }
    }
}
