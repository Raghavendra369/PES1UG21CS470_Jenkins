pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/Raghavendra369/PES1UG21CS470_Jenkins.git']]])
            }
        }
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './outp'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
