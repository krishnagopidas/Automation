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
        bat '''
            where docker
            "C:\\Users\\DELL\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" version
            "C:\\Users\\DELL\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t employee-management:v1 .
        '''
    }
}

    }
}
