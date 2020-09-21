
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
                echo 'Deploy Starts'
                sh 'docker run -dp 1000:3306 --env="MYSQL_ROOT_PASSWORD=root" --env="MYSQL_DB=test" mysql'
                echo 'Deploy Ends'
                
            }
        }
    }
}
