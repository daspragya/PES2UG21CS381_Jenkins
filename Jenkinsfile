pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PE2UG21CS381-1'
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
                echos 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
