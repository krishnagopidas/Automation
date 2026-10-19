pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checkout'
            }
        }

        stage('Maven Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t employee-management:v1 .'
            }
        }
    }
}
