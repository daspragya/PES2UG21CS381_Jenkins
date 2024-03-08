pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS381-1'
                sh 'g++ main.cpp -o output'
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                sh './output'
                echo 'Testing Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
