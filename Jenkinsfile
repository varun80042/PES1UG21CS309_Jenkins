pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS309-1'
                sh 'g++ main/newfile.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deployy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
